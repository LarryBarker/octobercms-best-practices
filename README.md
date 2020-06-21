<p align="center">
    <img src="https://d2f5cg397c40hu.cloudfront.net/website-static-files/images/october-color-logo-v1.svg" alt="OctoberCMS"/>

</p>
<p align="center">Beyond SOLID principles & patterns</p>

Here you'll find OctoberCMS best practices which tend to be overlooked in real life October projects.

### **Follow OctoberCMS naming conventions**

OctoberCMS does not follow traditional Laravel naming conventions for a number of reasons. As such, you should utilize the naming conventions accepted by the OctoberCMS community:

Follow naming conventions accepted by the OctoberCMS community:

What | How | Good | Bad
------------ | ------------- | ------------- | -------------
Controller | plural | Articles | ~~ArticlesController~~
Model | singular | User | ~~Users~~
hasOne or belongsTo relationship | singular | articleComment | ~~articleComments, article_comment~~
All other relationships | plural | articleComments | ~~articleComment, article_comments~~
Table name | author_plugin_ prefix, plural | acme_blog_article_comments | ~~article_comment, articleComments~~
Pivot table  | author_plugin_ prefix, semantically correct | acme_blog_user_articles | ~~article_users, articles_users~~
Boolean columns | is_prefix | is_active | ~~active~~
Migration | version folder heirarchy | 1.0.1/create_articles_table | ~~2017_01_01_000000_articles~~
Method | camelCase | getAll | ~~get_all~~
Controller method (regular) | match partial name | index | ~~saveArticle~~
Controller method (AJAX handler, specific method) | method prefix, camelCase | index_onDoSomething | ~~indexOnDoSomething~~
Controller method (AJAX global handler) | on prefix, TitleCase | onAjaxRequest
Controller YAML | snake_case | config_form.yaml | ~~configfields.yaml~~,~~fieldsconfig.yaml~~
Model YAML | columns/fields prefix, snake_case | columns_simple.yaml | ~~simplecolumns.yaml~~, ~~columnsposts.yaml~~
Controller partials | _prefix, snake_case, .htm extension | _users.htm | ~~users.htm~~
Class references | qualified namespace | \Backend\Behaviors\FormController::class | ~~'Backend.Behaviors.FormController'~~
Vendor naming | TitleCase | AcmeCo.SuperPlugin | ~~acme.blog~~, ~~rainLab.user~~

Also Follow [Laravel naming conventions](https://webdevetc.com/blog/laravel-naming-conventions) & [PSR standards](http://www.php-fig.org/psr/psr-2/) when possible.

### Foundation Library

[OctoberCMS](https://octobercms.com) is built on [Laravel](https://laravel.com).

### Learning OctoberCMS

The best place to learn about OctoberCMS is by [reading the documentation](https://octobercms.com/docs/setup/installation) or [following some tutorials](https://octobercms.com/support/articles/tutorials).

### Contact

* [Visit my site](https://larrybarker.me)
* [Check out my other repos](https://github.com/larrybarker)
* [Follow me on Twitter](https://twitter.com/thegreatbarker)
* [Find me on Slack](https://octobercms.slack.com/)

### Coding standards

Please follow the following guides and code standards:
* [Developer guidelines](https://octobercms.com/help/guidelines/developer)
* [PSR 4 Coding Standards](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md)
* [PSR 2 Coding Style Guide](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)
* [PSR 1 Coding Standards](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md)
