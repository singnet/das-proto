http_archive(
    name = "com_github_grpc_grpc",
    strip_prefix = "grpc-tags-v1.63.0",
    urls = [
        "https://github.com/grpc/grpc/archive/tags/v1.63.0.tar.gz",
    ],
)

load("@rules_cc//cc:defs.bzl", "cc_proto_library")
load("@rules_proto//proto:defs.bzl", "proto_library")
load("@com_github_grpc_grpc//bazel:cc_grpc_library.bzl", "cc_grpc_library")

cc_grpc_library(
    name = "attention_broker_cc_grpc",
    srcs = [":attention_broker_proto"],
    grpc_only = True,
    deps = [":attention_broker_cc_proto"],
    visibility = ["//visibility:public"],
)

cc_grpc_library(
    name = "common_cc_grpc",
    srcs = [":common_proto"],
    grpc_only = True,
    deps = [":common_cc_proto"],
    visibility = ["//visibility:public"],
)

cc_proto_library(
    name = "attention_broker_cc_proto",
    deps = [":attention_broker_proto"],
    visibility = ["//visibility:public"],
)

cc_proto_library(
    name = "common_cc_proto",
    deps = [":common_proto"],
    visibility = ["//visibility:public"],
)

proto_library(
    name = "attention_broker_proto",
    srcs = ["attention_broker.proto"],
    deps = [":common_proto"],
    visibility = ["//visibility:public"],
)

proto_library(
    name = "common_proto",
    srcs = ["common.proto"],
    visibility = ["//visibility:public"],
)

proto_library(
    name = "echo_proto",
    srcs = ["echo.proto"],
    visibility = ["//visibility:public"],
)
