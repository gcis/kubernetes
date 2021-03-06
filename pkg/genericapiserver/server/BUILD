package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "genericapiserver_test.go",
        "resource_config_test.go",
        "serve_test.go",
        "storage_factory_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/testapi:go_default_library",
        "//pkg/apis/extensions:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/generated/openapi:go_default_library",
        "//pkg/genericapiserver/registry/rest:go_default_library",
        "//pkg/storage/etcd/testing:go_default_library",
        "//vendor:github.com/go-openapi/spec",
        "//vendor:github.com/stretchr/testify/assert",
        "//vendor:k8s.io/apimachinery/pkg/api/meta",
        "//vendor:k8s.io/apimachinery/pkg/apimachinery",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/runtime/schema",
        "//vendor:k8s.io/apimachinery/pkg/runtime/serializer",
        "//vendor:k8s.io/apimachinery/pkg/util/net",
        "//vendor:k8s.io/apimachinery/pkg/util/sets",
        "//vendor:k8s.io/apimachinery/pkg/version",
        "//vendor:k8s.io/apiserver/pkg/authentication/user",
        "//vendor:k8s.io/apiserver/pkg/authorization/authorizer",
        "//vendor:k8s.io/apiserver/pkg/endpoints/request",
        "//vendor:k8s.io/apiserver/pkg/server/options",
        "//vendor:k8s.io/apiserver/pkg/storage/storagebackend",
        "//vendor:k8s.io/apiserver/pkg/util/flag",
        "//vendor:k8s.io/client-go/util/cert",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "config.go",
        "config_selfclient.go",
        "discovery.go",
        "doc.go",
        "genericapiserver.go",
        "healthz.go",
        "hooks.go",
        "resource_config.go",
        "resource_encoding_config.go",
        "serve.go",
        "storage_factory.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/genericapiserver/endpoints:go_default_library",
        "//pkg/genericapiserver/endpoints/filters:go_default_library",
        "//pkg/genericapiserver/endpoints/openapi:go_default_library",
        "//pkg/genericapiserver/registry/rest:go_default_library",
        "//pkg/genericapiserver/server/mux:go_default_library",
        "//pkg/genericapiserver/server/routes:go_default_library",
        "//vendor:github.com/coreos/go-systemd/daemon",
        "//vendor:github.com/emicklei/go-restful",
        "//vendor:github.com/emicklei/go-restful/swagger",
        "//vendor:github.com/go-openapi/spec",
        "//vendor:github.com/golang/glog",
        "//vendor:github.com/pborman/uuid",
        "//vendor:github.com/pkg/errors",
        "//vendor:gopkg.in/natefinch/lumberjack.v2",
        "//vendor:k8s.io/apimachinery/pkg/apimachinery",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/openapi",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/runtime/schema",
        "//vendor:k8s.io/apimachinery/pkg/runtime/serializer/recognizer",
        "//vendor:k8s.io/apimachinery/pkg/util/net",
        "//vendor:k8s.io/apimachinery/pkg/util/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/sets",
        "//vendor:k8s.io/apimachinery/pkg/util/validation",
        "//vendor:k8s.io/apimachinery/pkg/version",
        "//vendor:k8s.io/apiserver/pkg/admission",
        "//vendor:k8s.io/apiserver/pkg/authentication/authenticator",
        "//vendor:k8s.io/apiserver/pkg/authentication/authenticatorfactory",
        "//vendor:k8s.io/apiserver/pkg/authentication/request/union",
        "//vendor:k8s.io/apiserver/pkg/authentication/user",
        "//vendor:k8s.io/apiserver/pkg/authorization/authorizer",
        "//vendor:k8s.io/apiserver/pkg/authorization/authorizerfactory",
        "//vendor:k8s.io/apiserver/pkg/authorization/union",
        "//vendor:k8s.io/apiserver/pkg/endpoints/request",
        "//vendor:k8s.io/apiserver/pkg/server/filters",
        "//vendor:k8s.io/apiserver/pkg/server/healthz",
        "//vendor:k8s.io/apiserver/pkg/server/options",
        "//vendor:k8s.io/apiserver/pkg/storage/storagebackend",
        "//vendor:k8s.io/client-go/rest",
        "//vendor:k8s.io/client-go/util/cert",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//pkg/genericapiserver/server/mux:all-srcs",
        "//pkg/genericapiserver/server/openapi:all-srcs",
        "//pkg/genericapiserver/server/routes:all-srcs",
    ],
    tags = ["automanaged"],
)
