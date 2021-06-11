package(default_visibility = ["//visibility:public"])

load("@rules_proto//proto:defs.bzl", "proto_library")
load("@com_google_googleapis_imports//:imports.bzl", "go_proto_library")

proto_library(
    name = "intstr_proto",
    strip_import_prefix = "apimachinery-0.22.0-alpha.3/",
    import_prefix = "k8s.io/apimachinery/",
    srcs = [
        "apimachinery-0.22.0-alpha.3/pkg/util/intstr/generated.proto",
    ],
)

proto_library(
    name = "runtime_proto",
    strip_import_prefix = "apimachinery-0.22.0-alpha.3/",
    import_prefix = "k8s.io/apimachinery/",
    srcs = [
        "apimachinery-0.22.0-alpha.3/pkg/runtime/generated.proto",
    ],
)

proto_library(
    name = "runtime_schema_proto",
    strip_import_prefix = "apimachinery-0.22.0-alpha.3/",
    import_prefix = "k8s.io/apimachinery/",
    srcs = [
        "apimachinery-0.22.0-alpha.3/pkg/runtime/schema/generated.proto",
    ],
)

proto_library(
    name = "resource_proto",
    strip_import_prefix = "apimachinery-0.22.0-alpha.3/",
    import_prefix = "k8s.io/apimachinery/",
    srcs = [
        "apimachinery-0.22.0-alpha.3/pkg/api/resource/generated.proto",
    ],
)

proto_library(
    name = "meta_proto",
    strip_import_prefix = "apimachinery-0.22.0-alpha.3/",
    import_prefix = "k8s.io/apimachinery/",
    srcs = [
        "apimachinery-0.22.0-alpha.3/pkg/apis/meta/v1/generated.proto",
    ],
    deps = [
        ":runtime_proto",
        ":runtime_schema_proto"
    ],
)

go_proto_library(
    name = "intstr_go_proto",
    compilers = ["@io_bazel_rules_go//proto:go_grpc"],
    importpath = "k8s.io/apimachinery/pkg/util/intstr",
    protos = [":intstr_proto"],
)

go_proto_library(
    name = "runtime_go_proto",
    compilers = ["@io_bazel_rules_go//proto:go_grpc"],
    importpath = "k8s.io/apimachinery/pkg/runtime",
    protos = [":runtime_proto"],
)

go_proto_library(
    name = "runtime_schema_go_proto",
    compilers = ["@io_bazel_rules_go//proto:go_grpc"],
    importpath = "k8s.io/apimachinery/pkg/runtime/schema",
    protos = [":runtime_schema_proto"],
)

go_proto_library(
    name = "resource_go_proto",
    compilers = ["@io_bazel_rules_go//proto:go_grpc"],
    importpath = "k8s.io/apimachinery/pkg/api/resource",
    protos = [":resource_proto"],
)

go_proto_library(
    name = "meta_go_proto",
    compilers = ["@io_bazel_rules_go//proto:go_grpc"],
    importpath = "k8s.io/apimachinery/pkg/apis/meta/v1",
    protos = [":meta_proto"],
    deps = [
        ":runtime_go_proto",
        ":runtime_schema_go_proto",
    ],
)
