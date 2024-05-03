```jsx
searchParams: {
  [key: string]: string | string[] | undefined;
};
```
-  `?query=hello&query=world`
-  `{ query: [ 'hello', 'world' ] }`

<hr/>

#### input focus out `blur`

```diff
<Input
  disabled={isSearching}
  value={query}
  onChange={(e) => setQuery(e.target.value)}
  onKeyDown={(e) => {
    if (e.key === 'Enter') search();

+   if (e.key === 'Escape') {
+   inputRef.current?.blur();
+   }
  }}
  ref={inputRef}
  className='absolute inset-0 h-full'
/>
```

<hr/>

```js
// @ts-expect-error
// @ts-ignore
// @ts-check
// @ts-nocheck
```

<hr/>

#### [Github markdown diff](https://github.com/orgs/community/discussions/42489#discussioncomment-6702467)

```diff
+ Chelsea are going to be Premier League Champions 2023/2024
- Arsenal are going to be Premier League Champions 2023/2024
```

<hr/>

#### semantic search

<hr/>

#### experimental_taintObjectReference, experimental_taintUniqueValue

https://nextjs.org/docs/app/building-your-application/data-fetching/patterns#preventing-sensitive-data-from-being-exposed-to-the-client

#### expand vscode typescript ellipsis
https://github.com/microsoft/TypeScript/issues/26238#issuecomment-672086446


#### markdown

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.

#### gh https://cli.github.com/
```bash
gh repo create
```

```bash
git add -p -a
```