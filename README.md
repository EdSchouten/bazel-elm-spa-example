# The real world Elm example web application, built with Bazel

This repository contains a fork of
[Richard Feldman's Elm example application](https://github.com/rtfeldman/elm-spa-example),
modified to build with [the Bazel build system](https://bazel.build/).
It uses the [rules\_elm](https://github.com/EdSchouten/rules_elm)
package to build the Elm code. Bazel's official
[rules\_docker](https://github.com/bazelbuild/rules_docker) is used to
pack the resulting Javascript application and the static assets into
container layers. These are then combined into a container image based
on Nginx. This makes it easy to deploy and run this example application.

The advantage of using Bazel to build Elm code is that it makes it
possible to use a single build system to build, package and run tests
larger projects in one go. For example, if the Elm web application had
to communicate with a backend service written in Go, both of these could
easily be built and packaged into a Docker container through a uniform
build process.

To get more insight in how the Bazel build rules are structured,
consider [viewing the difference against `master`](https://github.com/EdSchouten/bazel-elm-spa-example/compare/master...EdSchouten:bazel).

## Building and using the Nginx container with the Elm web application

It should be sufficient to run the following command inside a checkout
of this repository on a system that has Bazel installed:

    bazel run :elm_spa_example_container

This will build the Elm web application, add it to a container image
based on Nginx and push it into the Docker daemon running on the current
system. It is then possible to launch this container as follows:

    docker run -p 80:80 bazel:elm_spa_example_container

**Tip:** The rules\_docker package provides a
[`container_push()`](https://github.com/bazelbuild/rules_docker#container_push)
function that allows you to directly push the resulting container image
into a remote registry. This function doesn't rely on the availability
of a local Docker daemon.

## Licensing terms

The changes made to this example web application are available under the
same license terms as the original web application (i.e., MIT).
