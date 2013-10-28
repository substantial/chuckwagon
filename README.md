# Chuckwagon

## What

Chuckwagon, the cowboy chef, rustles up production-deployable, using chef,
vagrant-hosted, development environments for your projects.

## Why

You want to develop your application in an environment as similar as
possible to your production environment. Chuckwagon makes this easier.

## How

### rails + mysql server

#### creating

If you already have the source code for your 'bbq blog' at ~/bbq-blog,
you would run the following to start creating an operating environment
ground for your production-like development environment:

Create a json file representing your rails+mysql environment in ~/bbq-blog-operations/.Chuckwagon:


```sh
chuckwagon new rails_mysql ~/bbq-blog-operations
```

This will create starter project, cloned from a known good state, with
rails and mysql. `~/bbq-blog-operations` is the location of the
"operating" repository for your project.

Now, configure your operations repository by replacing 'FIXME' with
values that work for your existing application.

Then run:

```sh
cd ~/bbq-blog-operations chuckwagon provision
```


#### operating

Starting your environment

```sh
cd ~/bbq-blog-operations && chuckwagon up
```

#### maintaining

As your application's needs grow, so can your chef recipes, Chuckwagon
sets up your knife-solo chef environment ready to grow.
