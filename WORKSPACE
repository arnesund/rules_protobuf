workspace(name = "org_pubref_rules_protobuf")


# ================================================================
# Go support requires rules_go
# ================================================================

git_repository(
    name = "io_bazel_rules_go",
    remote = "https://github.com/bazelbuild/rules_go.git",
    tag = "0.4.2", # Apr 7, 2017
)

load("@io_bazel_rules_go//go:def.bzl", "go_repositories")

go_repositories()


# ================================================================
# closure js_proto_library support requires rules_closure
# ================================================================

git_repository(
    name = "io_bazel_rules_closure",
    commit = "a6b65d5c5c9db8968fb8e03115d5e4f6976de8f7",
    remote = "https://github.com/bazelbuild/rules_closure.git",
)

load("@io_bazel_rules_closure//closure:defs.bzl", "closure_repositories")

closure_repositories()


# ================================================================
# csharp_proto_library support requires rules_dotnet (forked)
# ================================================================

git_repository(
    name = "io_bazel_rules_dotnet",
    commit = "ebc7c1cb61d45bd57042c60b6bfabdfff4979466",
    remote = "https://github.com/bazelbuild/rules_dotnet.git",
)

load("@io_bazel_rules_dotnet//dotnet:csharp.bzl", "csharp_repositories")

csharp_repositories(use_local_mono = False)


# ================================================================
# node_proto_library support requires rules_node
# ================================================================

git_repository(
    name = "org_pubref_rules_node",
    commit = "85b720f3d4299b0a1b9c7771c023352e9182045f",  # Oct 10, 2016
    remote = "https://github.com/pubref/rules_node.git",
)

load("@org_pubref_rules_node//node:rules.bzl", "node_repositories")

node_repositories()


# ================================================================
# Specific Languages Support
# ================================================================

load("//protobuf:rules.bzl", "proto_repositories")

proto_repositories()

load("//cpp:rules.bzl", "cpp_proto_repositories")

cpp_proto_repositories()

load("//csharp:rules.bzl", "csharp_proto_repositories")

csharp_proto_repositories()

load("//java:rules.bzl", "java_proto_repositories", "nano_proto_repositories")

java_proto_repositories()

nano_proto_repositories()

load("//go:rules.bzl", "go_proto_repositories")

go_proto_repositories()

load("//gogo:rules.bzl", "gogo_proto_repositories")

gogo_proto_repositories()

load("//grpc_gateway:rules.bzl", "grpc_gateway_proto_repositories")

grpc_gateway_proto_repositories()

load("//node:rules.bzl", "node_proto_repositories")

node_proto_repositories()

load("//objc:rules.bzl", "objc_proto_repositories")

objc_proto_repositories()

load("//python:rules.bzl", "py_proto_repositories")

py_proto_repositories()

load("//ruby:rules.bzl", "ruby_proto_repositories")

ruby_proto_repositories()


# ================================================================
# EXPERIMENTAL
# ================================================================


http_archive(
    name = "com_google_grpc",
    url = "https://github.com/grpc/grpc/archive/f5600e99be0fdcada4b3039c0f656a305264884a.zip", # Sep 1, 2017
    sha256 = "95ee013fdb605f9d4f47b1abcedc119f41d66d94ebc7af665c2866d4167e506e",
    strip_prefix = "grpc-f5600e99be0fdcada4b3039c0f656a305264884a",
)

new_http_archive(
    name = "com_github_c_ares_c_ares",
    url = "https://github.com/c-ares/c-ares/archive/7691f773af79bf75a62d1863fd0f13ebf9dc51b1.zip",
    sha256 = "ddce8def076a0a8cfa3f56595e391cf9e13a39fd4a7882822ed98cafd4079862",
    strip_prefix = "c-ares-7691f773af79bf75a62d1863fd0f13ebf9dc51b1",
    build_file_content = "",
)

load("//cpp:grpc_repository.bzl", "grpc_repository")

grpc_repository(
    name = "com_github_grpc_grpc",
)
