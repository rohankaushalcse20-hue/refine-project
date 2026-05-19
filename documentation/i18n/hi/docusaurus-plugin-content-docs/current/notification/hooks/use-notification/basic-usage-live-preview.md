```tsx live url=http://localhost:3000/products previewHeight=200px hideCode
setInitialRoutes(["/"]);
// visible-block-start
import { useNotification } from "@refinedev/core";
import { Button, Stack } from "@mui/material";

const ExamplePage: React.FC = () => {
  const { open, close } = useNotification();

  return (
    <Stack spacing={2} direction="row">
      <Button
        color="success"
        variant="outlined"
        size="small"
        onClick={() =>
          open?.({
            type: "success",
            message: "सफल",
            description: "कार्रवाई सफल रही",
          })
        }
      >
        सफल
      </Button>
      <Button
        color="error"
        variant="outlined"
        size="small"
        onClick={() =>
          open?.({
            type: "error",
            message: "त्रुटि",
            description: "कार्रवाई पूरी नहीं हो सकी",
          })
        }
      >
        त्रुटि
      </Button>

      <Button
        color="secondary"
        variant="outlined"
        size="small"
        onClick={() =>
          open?.({
            type: "progress",
            message: "प्रगति में",
            undoableTimeout: 5,
            cancelMutation: () => {
              alert("cancelMutation");
            },
          })
        }
      >
        प्रगति
      </Button>
    </Stack>
  );
};
// visible-block-end
render(
  <ReactRouter.BrowserRouter>
    <RefineMuiDemo resources={[]}>
      <ReactRouter.Routes>
        <ReactRouter.Route
          index
          element={
            <div style={{ padding: 24 }}>
              <ExamplePage />
            </div>
          }
        />
      </ReactRouter.Routes>
    </RefineMuiDemo>
  </ReactRouter.BrowserRouter>,
);
```
