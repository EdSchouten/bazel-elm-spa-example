load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "bazel_toolchains",
    sha256 = "4b1468b254a572dbe134cc1fd7c6eab1618a72acd339749ea343bd8f55c3b7eb",
    strip_prefix = "bazel-toolchains-d665ccfa3e9c90fa789671bf4ef5f7c19c5715c4",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/bazel-toolchains/archive/d665ccfa3e9c90fa789671bf4ef5f7c19c5715c4.tar.gz",
        "https://github.com/bazelbuild/bazel-toolchains/archive/d665ccfa3e9c90fa789671bf4ef5f7c19c5715c4.tar.gz",
    ],
)

http_archive(
    name = "build_bazel_rules_nodejs",
    sha256 = "fb87ed5965cef93188af9a7287511639403f4b0da418961ce6defb9dcf658f51",
    urls = ["https://github.com/bazelbuild/rules_nodejs/releases/download/0.27.7/rules_nodejs-0.27.7.tar.gz"],
)

http_archive(
    name = "com_github_edschouten_rules_elm",
    sha256 = "c34015356f755e5c8dd26c5a82ff9710353f925f435861892fb80a929fa07445",
    strip_prefix = "rules_elm-0.2",
    urls = ["https://github.com/EdSchouten/rules_elm/archive/v0.2.tar.gz"],
)

http_archive(
    name = "io_bazel_rules_docker",
    sha256 = "aed1c249d4ec8f703edddf35cbe9dfaca0b5f5ea6e4cd9e83e99f3b0d1136c3d",
    strip_prefix = "rules_docker-0.7.0",
    urls = ["https://github.com/bazelbuild/rules_docker/archive/v0.7.0.tar.gz"],
)

load("@io_bazel_rules_docker//repositories:repositories.bzl", container_repositories = "repositories")

container_repositories()

load("@io_bazel_rules_docker//container:container.bzl", "container_pull")

container_pull(
    name = "nginx_base",
    digest = "sha256:98efe605f61725fd817ea69521b0eeb32bef007af0e3d0aeb6258c6e6fe7fc1a",
    registry = "index.docker.io",
    repository = "library/nginx",
    tag = "1.15.9",
)

load("@com_github_edschouten_rules_elm//elm:deps.bzl", "elm_register_toolchains")

elm_register_toolchains()

load("@com_github_edschouten_rules_elm//repository:def.bzl", "elm_repository")

elm_repository(
    name = "elm_package_elm_browser",
    sha256 = "c4c3cb453bfe2dfc3a31f1760688d96e82d0bf091e00c99faadb8ed495dff5aa",
    strip_prefix = "browser-1.0.0",
    urls = ["https://github.com/elm/browser/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_core",
    sha256 = "9cfa20b6468b8bfb4f02c6652f43de1dd1c58b328060830ab804964da0417982",
    strip_prefix = "core-1.0.0",
    urls = ["https://github.com/elm/core/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_explorations_markdown",
    sha256 = "dee4da750f4cdb7c48f021775c4ccad727a8f853f4b639f7709c13d52308614c",
    strip_prefix = "markdown-1.0.0",
    urls = ["https://github.com/elm-explorations/markdown/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_explorations_test",
    sha256 = "1233c0cb3d663630b939edb058d904e1275dfae0813ddf0bb63459d0cdf8bfe9",
    strip_prefix = "test-1.2.1",
    urls = ["https://github.com/elm-explorations/test/archive/1.2.1.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_html",
    sha256 = "73b885e0a3d2f9781b1c9bbcc1ee9ac032f503f5ef46a27da3ba617cebbf6fd8",
    strip_prefix = "html-1.0.0",
    urls = ["https://github.com/elm/html/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_http",
    sha256 = "88ea7bdeaefc56631aeb0e024ae4133d60aafa7caa23195694f9531513aaf5c5",
    strip_prefix = "http-1.0.0",
    urls = ["https://github.com/elm/http/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_json",
    sha256 = "cbba2f0ea00fc83f5781207a7de1d49f5a1ad6ed3ce578f218060b87a75310bc",
    strip_prefix = "json-1.0.0",
    urls = ["https://github.com/elm/json/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_parser",
    sha256 = "8c1fd91229a45edddcf981ac2a06d2c9f19a21a07a2ffe37e66a670a06a69f4c",
    strip_prefix = "parser-1.0.0",
    urls = ["https://github.com/elm/parser/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_random",
    sha256 = "b4b9dc99d5a064bc607684dd158199208bce51c0521b7e8a515c365e0a11168d",
    strip_prefix = "random-1.0.0",
    urls = ["https://github.com/elm/random/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_time",
    sha256 = "e18bca487adec67bfe4043a33b975d81527a7732377050d0421dd86d503c906d",
    strip_prefix = "time-1.0.0",
    urls = ["https://github.com/elm/time/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_url",
    sha256 = "840e9d45d8a9bd64a7f76421a1de2518e02c7cbea7ed42efd380b4e875e9682b",
    strip_prefix = "url-1.0.0",
    urls = ["https://github.com/elm/url/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_elm_virtual_dom",
    sha256 = "5899564798629e91ef95238f8ba7f4d40260d18496b622469d69fc03457aa842",
    strip_prefix = "virtual-dom-1.0.0",
    urls = ["https://github.com/elm/virtual-dom/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_noredink_elm_json_decode_pipeline",
    sha256 = "d4c272a21626a02f8e782929e74def3ee04e1e0431741f1eed0287ee81ed4578",
    strip_prefix = "elm-json-decode-pipeline-1.0.0",
    urls = ["https://github.com/NoRedInk/elm-json-decode-pipeline/archive/1.0.0.tar.gz"],
)

elm_repository(
    name = "elm_package_rtfeldman_elm_iso8601_date_strings",
    sha256 = "3e78b642298e483584f6c4938e00649fbe550680126e9717f58a281d125bc5fb",
    strip_prefix = "elm-iso8601-date-strings-1.1.0",
    urls = ["https://github.com/rtfeldman/elm-iso8601-date-strings/archive/1.1.0.tar.gz"],
)

load("@build_bazel_rules_nodejs//:defs.bzl", "node_repositories")

node_repositories()
