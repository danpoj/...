```jsx
searchParams: {
  [key: string]: string | string[] | undefined;
};
```
`string[]`이 어디서 왔나 했더니 `?query=hello&query=world`같은 key값으로 보내면 배열`{ query: [ 'hello', 'world' ] }`로 온다

<hr/>

```jsx
<Input
  disabled={isSearching}
  value={query}
  onChange={(e) => setQuery(e.target.value)}
  onKeyDown={(e) => {
    if (e.key === 'Enter') search();

  + if (e.key === 'Escape') {
  +  inputRef.current?.blur();
  +}
  }}
  ref={inputRef}
  className='absolute inset-0 h-full'
/>
```