package(default_visibility = ["//visibility:public"])

load("@rules_proto//proto:defs.bzl", "proto_library")
load("@com_google_googleapis_imports//:imports.bzl", "go_proto_library")

proto_library(
    name = "core_proto",
    strip_import_prefix = "api-0.21.1/",
    import_prefix = "k8s.io/api/",    
    srcs = [
		"api-0.21.1/core/v1/generated.proto",
    ],
    deps = [
        "@io_kubernetes_apimachinery//:meta_proto",
		    "@io_kubernetes_apimachinery//:resource_proto",
		    "@io_kubernetes_apimachinery//:intstr_proto",
		    "@io_kubernetes_apimachinery//:runtime_proto",
		    "@io_kubernetes_apimachinery//:runtime_schema_proto",
    ],
)

go_proto_library(
    name = "core_go_proto",
    compilers = ["@io_bazel_rules_go//proto:go_grpc"],
    importpath = "k8s.io/api/core/v1",
    protos = [":core_proto"],
    deps = [
		    "@io_kubernetes_apimachinery//:meta_go_proto",
		    "@io_kubernetes_apimachinery//:resource_go_proto",
		    "@io_kubernetes_apimachinery//:intstr_go_proto",
        "@io_kubernetes_apimachinery//:runtime_go_proto",
        "@io_kubernetes_apimachinery//:runtime_schema_go_proto",
    ],
)