<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ably live provider example

यह example दिखाता है कि real-time resources के लिए **Refine** को Ably के साथ कैसे इस्तेमाल किया जाता है। `liveProvider` lists और detail views को events पर react करने देता है, जबकि resources और providers की structure बनी रहती है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example live-provider-ably
```

## मुख्य बिंदु

- `liveProvider` की configuration
- Ably के साथ real-time events
- resources को Refine update flow से जोड़ना
- commands और links को original example जैसा रखना

[live-provider-ably example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/live-provider-ably?view=preview&theme=dark&codemirror=1)
