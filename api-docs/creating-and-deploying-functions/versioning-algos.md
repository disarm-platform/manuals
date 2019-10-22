# Versioning algos

Two parts needed: 1. Edit the `stack.yml` file, to change the `image` entry:

* from: 

  ```text
  provider:
  name: faas
  gateway: https://faas.srv.disarm.io
  functions:
  fn-covariate-extractor:
    lang: dockerfile
    handler: ./fn-covariate-extractor
    image: disarm/fn-covariate-extractor:0.0.3
  ```

* to \(check different last line!\):

  ```text
  provider:
  name: faas
  gateway: https://faas.srv.disarm.io
  functions:
  fn-covariate-extractor:
    lang: dockerfile
    handler: ./fn-covariate-extractor
    image: disarm/fn-covariate-extractor:0.0.4
  ```

  1. Create a matching tag in Git \(using SourceTree, Fork, etc - or via command line `git tag v0.0.4`\). This tag needs to be created _after_ you've committed the version 'bump' in step 1.

1. Then remember to push \(including the tags!\)    
