<h1 align="center">Redux + TS Notes</h1>

In a normal Redux project, it is worth the time to think about the design of our store before writing code.

In a TS project, it is recommended to think about design first.

## Redux `store` Design

Searching `npm` : `registry.npmjs.org/-/v1/search?text=userinput`

### High level project idea

1. We're fetching packages from NPM.
2. `package` is a reserved keyword in Typescript.
3. We're going to call NPM packages `repositories`.

### Redux `store`

`repositories`

- `data` : List of repositories from NPM
- `loading` : True or False whether we're fetching `data`
- `error` : String, error message if one occurred during fetch

### `Actions`

#### Action Creator

- `searchRepositories(name)`

#### Actions

- `SearchRepositories`
- `SearchRepositoriesSuccess`
- `SearchRepositoriesError`

#### Action Types

- `search_repositories`
- `search_repositories_success`
- `search_repositories_error`

## Directory Structure

```
|-src/
|----/components
|--------/App.tsx
|--------/RepositoriesList.tsx
|----/redux
|--------/index.ts
|--------/reducers
|--------/action_creators
|--------/middlewares
```

`index.ts` imports all redux related stuff and re-exports.
