```tsx live url=http://localhost:3000/categories previewHeight=300px
import React from "react";
import { Refine } from "@refinedev/core";

setInitialRoutes(["/posts"]);
// visible-block-start
import React from "react";
import { useInfiniteList } from "@refinedev/core";

const PostList = () => {
  const {
    result: { data, hasNextPage, hasPreviousPage },
    query: { isError, isLoading, fetchNextPage, isFetchingNextPage },
  } = useInfiniteList({
    resource: "categories",
    pagination: {
      pageSize: 4,
    },
  });

  if (isLoading) {
    return <p>लोड हो रहा है</p>;
  }
  if (isError) {
    return <p>कुछ गलत हो गया</p>;
  }

  const allPages = [].concat(...(data?.pages ?? []).map((page) => page.data));

  return (
    <div>
      <ul>
        {allPages.map(({ id, title }) => (
          <li key={id}>
            {id}.{title}
          </li>
        ))}
      </ul>
      {hasNextPage && (
        <button onClick={() => fetchNextPage()} disabled={isFetchingNextPage}>
          {isFetchingNextPage ? "और लोड हो रहा है..." : "और लोड करें"}
        </button>
      )}
    </div>
  );
};
// visible-block-end

setRefineProps({
  // Layout: (props: LayoutProps) => <Layout {...props} />,
  resources: [
    {
      name: "posts",
      list: "/posts",
    },
  ],
});

render(
  <ReactRouter.BrowserRouter>
    <RefineHeadlessDemo>
      <ReactRouter.Routes>
        <ReactRouter.Route path="/posts" element={<PostList />} />
      </ReactRouter.Routes>
    </RefineHeadlessDemo>
  </ReactRouter.BrowserRouter>,
);
```
