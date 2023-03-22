workspace(name = "envoy_pb")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")

# Google protobuf
http_archive(
    name = "rules_proto",
    sha256 = "dc3fb206a2cb3441b485eb1e423165b231235a1ea9b031b4433cf7bc1fa460dd",
    strip_prefix = "rules_proto-5.3.0-21.7",
    urls = [
        "https://github.com/bazelbuild/rules_proto/archive/refs/tags/5.3.0-21.7.tar.gz",
    ],
)
load("@rules_proto//proto:repositories.bzl", "rules_proto_dependencies", "rules_proto_toolchains")
rules_proto_dependencies()
rules_proto_toolchains()

# Google protobuf: Well Known Types Proto Library
git_repository(
    name = "com_google_protobuf",
    remote = "https://github.com/protocolbuffers/protobuf",
    # 2022-12-14.
    tag = "v21.12",
)

"""
http_archive(
    name = "com_google_protobuf",
    sha256 = "52b6160ae9266630adb5e96a9fc645215336371a740e87d411bfb63ea2f268a0",
    strip_prefix = "protobuf-3.18.0",
    urls = [
      "https://github.com/protocolbuffers/protobuf/releases/download/v3.18.0/protobuf-all-3.18.0.tar.gz"
    ],
),
"""

git_repository(
    name = "com_github_cncf_udpa",
    remote = "https://github.com/cncf/xds",
    # 2023-01-12.
    commit = "46e39c7b9b4321731ebe247f2e176fdf0518d76e",
)
