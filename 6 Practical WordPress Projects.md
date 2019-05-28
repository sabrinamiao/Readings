# 6 Practical WordPress Projects

## Chapter 1 How to Build a WordPress Theme from Scratch

### A Word or Two on the Basics

WordPress was conceived as a blog engine, or a simple, blogging-oriented content management system.
It was initially released in 2003, by Matt Mullenweg and Mike Little.
WordPress is a PHP-powered web application that uses MySQL as its database, and is usually run behind a server program, such as NGINX or Apache.

### Basic template and Partials Files

The minimum `index.php` file catches all the queries that don't have their respective specialized template files within a theme.
`front-page.php`, `home.php`, `page.php`, `taxonomy.php`, `author.php`, `archive.php` are some of the templates that we can use in our themes to further structure specific pages or queries in our theme.

**Partials files** encapsulate repeatable parts of pages in WordPress website.

### Template Hierarchy

In the WordPress templating system, there's a hierarchy of template files that WordPress will try to use for each request.

To explain this on a page request - when the visitor visits a specific page on a WordPress website - WordPress will first try to find the template the page author assigned to it in the `wp-admin` backend.
That can be a completely custom template file, even completely static.
If there's no such template, or it wasn't assigned, WordPress will try to find a template file with a \_slug+ of that particular page in its filename.
That would look like `page-mypageslug.php` - whatever our `mypageslug` may be.
The next file WordPress will try to use will be a file with that particular page's ID in its filename - like `page-48.php`.
If none of those page-specific files exist, WordPress will try to use `page.php` - used for **all** the **pages**, unless otherwise specified.
If it doesn't find `page.php`, it will try to use `singular.php`.
This template file is used when - for posts - `single.php` is not found, and for pages when `page.php` is not found.
If none of these are found in our page request example, WordPress will fall back to `index.php`.

### WordPress Post Types

The content in WordPress exists in the form of post types.
The built-in types are posts and pages.
WordPress also has a built-in attachment post type, navigation menus and revisions.

To specify own post types, whether in our themes or our plugins, we need to use the `register_post_type($post_type, $args)`.

### WordPress Action and Filter Hooks

In the process of execution of the page connected to visitor's web request, there are certain registered points - hooks - that enable us to fire actions at those points.

We hook PHP functions to those points to be executed. Those are action hooks.

Filter hooks are focused on processing - changing - pieces of data within the execution cycle.

### The Loop

The Loop is the elementary part of the WordPress request cycle.
The Loop is PHP code used by WordPress to display posts.
Using The Loop, WordPress processes each psot to be displayed on the current page, and formats it according to how it matches specified criteria within The Loop tags.

### Conditional Tags

WordPress Conditional Tags are snippets of PHP code that enable us to display pieces of content only when certain conditions are satisfied.
