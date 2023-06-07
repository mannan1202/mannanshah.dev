---
title: 'Conditional useQuery in React Query'
description: 'conditionally managing api calls using react query'
pubDate: 2023-06-07
---

Learning by doing and experimenting with different tools and technologies can be a great way to discover new features and ways of doing things that you may not have known otherwise. In my case, while transitioning from Vue.js 2 to React, I stumbled upon React Query, which I instantly fell in love with for its ease of use and excellent documentation.

One challenge I faced was running the query conditionally, but after reading the documentation, I discovered that I could use **`useQuery`** as a function and call it conditionally based on my requirements. This was a great discovery for me, as it allowed me to have better control over when to run the query.

```jsx
const goodDog = true || false;
useQuery(['dog'], giveTreat(), { enabled: condition });
```

That’s it, `useQuery` will only work when enabled is true. Cheers
