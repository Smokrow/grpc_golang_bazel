load("@rules_proto_grpc//go:defs.bzl", "go_proto_library")
load("@rules_proto//proto:defs.bzl", "proto_library")

proto_library(
   name = "test_proto",
   srcs = ["messages.proto"],
   visibility = ["//visibility:public"]
)

go_proto_library(
    name = "test_go_library",
    go_deps = [
        "@com_github_golang_protobuf//ptypes/any:go_default_library",
    ],
    importpath = "proto/messages",
    deps = [":test_proto"],
    visibility = ["//visibility:public"]
)
