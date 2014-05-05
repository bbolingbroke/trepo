# Trepo
A Genealogical API built on [vGraph](https://github.com/trepo/vgraph), [dCap](https://github.com/trepo/dcap), [pTree](https://github.com/trepo/ptree), and [nPipes](https://github.com/trepo/npipes).

![](img/stack.png)

## Versioning

**Current Version** // TODO

We use [semver](http://semver.org/) versioning via the `Accept-Version` header.

[spec](spec/versioning.md)

## REST-ish
Yup. Deal with it. [Read more](http://en.wikipedia.org/wiki/Representational_state_transfer).

## JSON
Its the only music we ever play.
Don't know about JSON? [Read about it here](http://www.json.org/).
And yes, [JSONP](http://en.wikipedia.org/wiki/JSONP) is supported.
// TODO [maybe put meta info in the callback](https://developer.github.com/v3/#json-p-callbacks)? 

This means no XML. Welcome to the 21st century.

## Auth
Standard token based authentication in the header. 

[spec](spec/auth.md)

## Rate Limiting
// TODO

# API Sections

## Info
Mounted at `/`, this provides version information.

[spec](spec/root.md)

## Graph
Mounted at `/graph`, this provides access to the underlying local pTree implementation and provides read, write, update, and delete operations.

[spec](spec/graph)

## Query
Mounted at `/query`, this provides generalized access to pTree, and utilizes nPipes to perform queries across various repositories. It exposes things like generational, family, and validation queries.

[spec](spec/query)

## Search
// TODO combine with Query?
Mounted at `/search`, this provides search functionality across pTree, such as place, surname, and other searches.

[spec](spec/search)

## Commit
Mounted at `/commit`, this provides commit related functionality such as manual commits, commit history, and commit searching.

[spec](spec/commit)

## Patch
Mounted at `/patch`, this provides the ability to patch vGraph with commits.

[spec](spec/patch)