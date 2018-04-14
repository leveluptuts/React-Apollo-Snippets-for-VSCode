# React Apollo Snippets

## Installation

1.  Open the extensions sidebar on Visual Studio Code
2.  Search for **React Apollo Snipets**
3.  Click **Install** to install it.
4.  Click **Reload** to reload the your editor
5.  Enjoy

## Snippets

### Imports

| prefix | snippet                                         |
| ------ | ----------------------------------------------- |
| iap    | import { ApolloProvider } from 'react-apollo';  |
| iaq    | import { Query } from 'react-apollo';           |
| iam    | import { Mutation } from 'react-apollo';        |
| iaqm   | import { Query, Mutation } from 'react-apollo'; |
| iac    | import { ApolloConsumer } from 'react-apollo';  |

### Components

#### am

```
<Mutation
  mutation={MUTATION_CONST}
>
  {mutationName => (

  )}
</Mutation>
```

#### aq

```
<Query query={QUERY_CONST}>
  {({ data }) => (
    {data}
  )}
</Query>
```

#### aqf

```
<Query query={QUERY_CONST}>
  {({ loading, error, data }) => {
    if (loading) return "Loading...";
    if (error) return `Error! ${error.message}`;
    return (
      {data}
    );
  }}
</Query>
```

#### amrf

```
<Mutation
  mutation={MUTATION_CONST}
  refetchQueries={['queryName']}
>
  {mutationName => (

  )}
</Mutation>
```

#### amrb

```
<Mutation
  mutation={MUTATION_CONST}
>
  {$1:mutationName => <button onClick={mutationName}>$2</button>}
</Mutation>
```

#### amrb

```
<ApolloConsumer>
  {cache => (
    <Button
      onClick={() => cache.writeData({ data: { $1: $2 } })}
    >
      $3
    </Button>
  )}
</ApolloConsumer>
```

#### ap

```
<ApolloProvider client={client}>
  <App />
</ApolloProvider>
```

## Sponsorship

This plugin is sponsored by [Level Up Tutorials](https://www.leveluptutorials.com/)

[![Level Up Tutorials Logo](images/logo.png)](https://www.leveluptutorials.com/)

[Level Up Tutorials on Youtube](https://www.youtube.com/user/LevelUpTuts)

[Level Up Tutorials on Instagram](https://www.instagram.com/leveluptutorials/)

Please consider becoming a pro subscriber or purchasing a tutorial series to help support Level Up Tutorials

## Contribute

I'm happy to accept PRs for snippets that are wanted. I primarily made this for snippets that I personally use frequently and am probably missing some important ones.
