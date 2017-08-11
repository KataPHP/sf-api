Kata API
========

Installation
-----------

```bash
$ git clone git@github.com:KataPHP/sf-api.git
$ cd sf-api
$ docker-compose up -d
```

Open http://127.0.0.1:8085/ and create a new database named **kata**

```bash
$ composer install
$ bin/console server:start
```

Instruction
-----------

1. Create Entity
    - Create an Entity article
        - ID ([uuid])
        - Title
        - Slug (Based on title [sluggable])
        - Content
        - Author
        - CreatedAt ([timestampable])
        - UpdatedAt ([timestampable])
    - Add [fixtures] to create 20 articles

2. Create Controller

Add ArticleController ([API Response Code],  All routes returns json) :
* add cgetAction() (method GET, route /article) to retrive all articles
* add getAction() (method GET, route /article/{slug}) to retrive an article via uuid or slug
* add newAction() (method POST, route /article) to create a new article
* add removeAction() (method DELETE, route /article/{slug}) to delete an article via uuid or slug
* add updateAction() (method PUT, route /article/{slug}) to update an article


[fixtures]: https://github.com/hautelook/AliceBundle#installation
[sluggable]: https://github.com/Atlantic18/DoctrineExtensions/blob/master/doc/sluggable.md
[timestampable]: https://github.com/Atlantic18/DoctrineExtensions/blob/master/doc/timestampable.md
[uuid]: https://github.com/ramsey/uuid-doctrine
[API Response Code]:https://gist.github.com/subfuzion/669dfae1d1a27de83e69