```jsx
searchParams: {
  [key: string]: string | string[] | undefined;
};
```
`string[]`이 어디서 왔나 했더니 key값 같은경우 string 배열로 온다 
- in `?query=hello&query=world`
- out `{ query: [ 'hello', 'world' ] }`

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



