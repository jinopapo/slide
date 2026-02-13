---
marp: true
theme: myTheme
---
## コード例タイトル
```ts
type User = {
  id: number
  name: string
}

const users: User[] = [
  { id: 1, name: 'Alice' },
  { id: 2, name: 'Bob' },
]

const names = users.map((u) => u.name)
console.log(names)
```
