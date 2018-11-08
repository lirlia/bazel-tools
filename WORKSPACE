workspace(name = "com_github_atlassian_bazel_tools")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "f87fa87475ea107b3c69196f39c82b7bbf58fe27c62a338684c20ca17d1d8613",
    urls = ["https://github.com/bazelbuild/rules_go/releases/download/0.16.2/rules_go-0.16.2.tar.gz"],
)

http_archive(
    name = "bazel_gazelle",
    sha256 = "6e875ab4b6bf64a38c352887760f21203ab054676d9c1b274963907e0768740d",
    urls = ["https://github.com/bazelbuild/bazel-gazelle/releases/download/0.15.0/bazel-gazelle-0.15.0.tar.gz"],
)

http_archive(
    name = "com_github_bazelbuild_buildtools",
    sha256 = "e4c83a7a5d0712e2cea2077112a5eb6bb1af75a84e34c8c9b77330e322966b8b",
    strip_prefix = "buildtools-e90e7cc6ef3e6d08d4ca8a982935c3eed638e058",
    urls = ["https://github.com/bazelbuild/buildtools/archive/e90e7cc6ef3e6d08d4ca8a982935c3eed638e058.tar.gz"],
)

load("@io_bazel_rules_go//go:def.bzl", "go_register_toolchains", "go_rules_dependencies")
load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")
load("@com_github_bazelbuild_buildtools//buildifier:deps.bzl", "buildifier_dependencies")

go_rules_dependencies()

go_register_toolchains()

gazelle_dependencies()

buildifier_dependencies()
