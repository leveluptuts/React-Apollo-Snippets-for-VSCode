# React Apollo Snippets

[![Version](https://vsmarketplacebadge.apphb.com/version/leveluptutorials.react-apollo-snippets.svg)](https://marketplace.visualstudio.com/items?itemName=leveluptutorials.react-apollo-snippets)

This plugin is sponsored by [Level Up Tutorials](https://www.leveluptutorials.com/)

## Installation

1.  Open the extensions sidebar on Visual Studio Code
2.  Search for **React Apollo Snipets**
3.  Click **Install** to install it.
4.  Click **Reload** to reload the your editor
5.  Enjoy

## Snippets

### Imports

| prefix | snippet                                               |
| ------ | ----------------------------------------------------- |
| iap    | import { ApolloProvider } from 'react-apollo';        |
| iaq    | import { Query } from 'react-apollo';                 |
| iam    | import { Mutation } from 'react-apollo';              |
| iaqm   | import { Query, Mutation } from 'react-apollo';       |
| iauq   | import { useQuery } from 'react-apollo';              |
| iaum   | import { useMutation } from 'react-apollo';           |
| iauqm  | import { useQuery, useMutation } from 'react-apollo'; |
| iac    | import { ApolloConsumer } from 'react-apollo';        |

### Components

#### aq

##### Apollo Query Simple

```
<Query query={QUERY_CONST}>
  {({ data }) => (
    {data}
  )}
</Query>
```

#### aqf

##### Apollo Query Full

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

#### am

##### Apollo Mutation Simple

```
<Mutation
  mutation={MUTATION_CONST}
>
  {mutationName => (

  )}
</Mutation>
```

#### amrf

##### Apollo Mutation Refetch Queries

```
<Mutation
  mutation={MUTATION_CONST}
  refetchQueries={['queryName']}
>
  {mutationName => (

  )}
</Mutation>
```

#### amb

##### Apollo Mutation Button

```
<Mutation
  mutation={MUTATION_CONST}
>
  {$1:mutationName => <button onClick={mutationName}>$2</button>}
</Mutation>
```

#### asm

##### Apollo State Mutation

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

##### Apollo Provider

```
<ApolloProvider client={client}>
  <App />
</ApolloProvider>
```

> From v3 react apollo started supporting hooks, we library supports them.

### Hooks

#### uq

##### Apollo useQuery Simple

```
const { data } = useQuery(QUERY_CONST);
```

#### uqf

##### Apollo useQuery Full

```
const {error, data, loading} = useQuery(QUERY_CONST, { variables: {} });
    if (loading) return "Loading...";
    if (error) return `Error! ${error.message}`;
```

#### um

##### Apollo useMutation Simple

```
const [mutationFn] = useMutation(MUTATION_CONST, { variables: {} });
```

#### umrf

##### Apollo useMutation Refetch Queries

```
const [mutationFn, {error, data, loading}] = useMutation(MUTATION_CONST, { variables: {}, refetchQueries: [QUERY_CONST] });
```

#### uc

##### Apollo Client

```
const client = useApolloClient();
```

## Sponsorship

This plugin is sponsored by [Level Up Tutorials](https://www.leveluptutorials.com/)

[![Level Up Tutorials Logo](images/logo.png)](https://www.leveluptutorials.com/)

[Level Up Tutorials on Youtube](https://www.youtube.com/user/LevelUpTuts)

[Level Up Tutorials on Instagram](https://www.instagram.com/leveluptutorials/)

Please consider becoming a pro subscriber or purchasing a tutorial series to help support Level Up Tutorials

## Contribute

I'm happy to accept PRs for snippets that are wanted. I primarily made this for snippets that I personally use frequently and am probably missing some important ones.
