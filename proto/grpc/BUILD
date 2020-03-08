load("@rules_proto_grpc//go:defs.bzl", "go_proto_library")
load("@rules_proto//proto:defs.bzl", "proto_library")

proto_library(
   name = "grpc_proto",
   srcs = ["grpc.proto"],
   deps = ["//proto/messages:test_proto"],
)

go_proto_library(
    name = "grpc_go_library",
    go_deps = [
        "@com_github_golang_protobuf//ptypes/any:go_default_library",
	"//proto/messages:test_go_library"
    ],
    importpath = "proto/Services",
    deps = [":grpc_proto",
	    "//proto/messages:test_proto"],
    visibility = ["//visibility:public"]
)
