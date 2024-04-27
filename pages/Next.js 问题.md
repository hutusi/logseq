title:: Next.js 问题

-
- ## call API route 404
- 参考[Vercel AI SDK](https://sdk.vercel.ai/docs/getting-started) 写了个API route，但调用时总报404：
- ```
  POST http://localhost:3000/api/chat 404 (Not Found)
  ```
-
- 后来发现是在配置文件 next.config.mjs 里：
- ```ts
  const nextConfig = {
    output: "export",
  };
  ```
- 将output这一行注释或删掉就OK了，没明白是什么原因导致的，可能跟这个配置生成静态网站有关。
-
-
-