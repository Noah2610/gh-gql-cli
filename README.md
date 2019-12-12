# gh-gql-cli
__GitHub GraphQL API helper script__.  
Simplifies sending GraphQL requests to GitHub's API endpoint,  
using `curl` with your query files.

## Installation
__TODO:__ Provide as `zip` releases.  

Clone the repository ...
```
git clone https://github.com/Noah2610/gh-gql-cli
```
and run the script in the cloned directory, after `cd gh-gql-cli` into it ...
```
./gh-gql-cli --help
```

## Usage
```
./gh-gql-cli --help
```
```
DESCRIPTION
    ./gh-gql-cli - Helper script for sending graphql queries to GitHub.

USAGE
    ./gh-gql-cli [OPTIONS] QUERY_FILE

ARGUMENTS
    QUERY_FILE
        Path to a file containing a graphql query.

OPTIONS
    --help, -h
        Prints this usage text and exits.

    --token-file, -T <TOKEN_FILE>
        Path to a file containing your GitHub token.
        The GitHub token is necessary for queries.
        Optional; defaults to ./GH_TOKEN when omitted.
        Generate your token from your GitHub account's settings page under:
            Developer settings -> Personal access tokens
            https://github.com/settings/tokens

    --token, -t <TOKEN>
        Pass your GitHub token on the command-line with this option.
        NOT RECOMMENDED: It's unsafe to type secrets on the command-line this.
        Prefer --token-file option.

EXAMPLES
    # Run the query in the file "./my-query.graphql",
    # using the GitHub token in the file "./my-gh-token"
    ./gh-gql-cli --token-file ./my-gh-token ./my-query.graphql
    # Equivalent:
    ./gh-gql-cli -T ./my-gh-token ./my-query.graphql

NOTES
    If you have jq installed, then the JSON output
    returned from the query request will be prettified using jq.
    https://stedolan.github.io/jq

    GitHub's graphql API preview feature deletePackageVersion is enabled with this script.
    https://developer.github.com/v4/mutation/deletepackageversion
```

## License
Distributed under the terms of the [MIT License][mit].

[mit]: https://github.com/Noah2610/gh-gql-cli/blob/master/LICENSE
