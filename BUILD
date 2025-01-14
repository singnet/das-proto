#load("@rules_cc//cc:defs.bzl", "cc_proto_library")
#load("@rules_proto//proto:defs.bzl", "proto_library")

#load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")
#grpc_deps()
#load("@com_github_grpc_grpc//bazel:grpc_extra_deps.bzl", "grpc_extra_deps")
#grpc_extra_deps()

load("@com_github_grpc_grpc//bazel:cc_grpc_library.bzl", "cc_grpc_library")

package(default_visibility = ["//visibility:public"])

cc_grpc_library(
    name = "attention_broker_cc_grpc",
    srcs = [":attention_broker_proto"],
    grpc_only = True,
    deps = [":attention_broker_cc_proto"],
)

cc_grpc_library(
    name = "atom_space_node_cc_grpc",
    srcs = [":atom_space_node_proto"],
    grpc_only = True,
    deps = [":atom_space_node_cc_proto"],
)

cc_grpc_library(
    name = "common_cc_grpc",
    srcs = [":common_proto"],
    grpc_only = True,
    deps = [":common_cc_proto"],
)

cc_proto_library(
    name = "attention_broker_cc_proto",
    deps = [":attention_broker_proto"],
)

cc_proto_library(
    name = "atom_space_node_cc_proto",
    deps = [":atom_space_node_proto"],
)

cc_proto_library(
    name = "common_cc_proto",
    deps = [":common_proto"],
)

proto_library(
    name = "attention_broker_proto",
    srcs = ["attention_broker.proto"],
    deps = [":common_proto"],
)

proto_library(
    name = "atom_space_node_proto",
    srcs = ["atom_space_node.proto"],
    deps = [":common_proto"],
)

proto_library(
    name = "common_proto",
    srcs = ["common.proto"],
)

proto_library(
    name = "echo_proto",
    srcs = ["echo.proto"],
)

