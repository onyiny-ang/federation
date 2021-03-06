load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "aes_gcm.go",
        "aes_gcm_content_cipher.go",
        "cipher.go",
        "cipher_builder.go",
        "cipher_util.go",
        "decryption_client.go",
        "doc.go",
        "encryption_client.go",
        "envelope.go",
        "hash_io.go",
        "helper.go",
        "key_handler.go",
        "kms_key_handler.go",
        "mat_desc.go",
        "strategy.go",
    ],
    importpath = "github.com/aws/aws-sdk-go/service/s3/s3crypto",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/aws/aws-sdk-go/aws:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/aws/awserr:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/aws/client:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/aws/request:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/service/kms:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/service/kms/kmsiface:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/service/s3:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/service/s3/s3iface:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "aes_gcm_test.go",
        "cipher_util_test.go",
        "hash_io_test.go",
        "helper_test.go",
        "key_handler_test.go",
        "kms_key_handler_test.go",
        "mat_desc_test.go",
    ],
    importpath = "github.com/aws/aws-sdk-go/service/s3/s3crypto",
    library = ":go_default_library",
    deps = [
        "//vendor/github.com/aws/aws-sdk-go/aws:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/awstesting/unit:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/service/kms:go_default_library",
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
    ],
)

go_test(
    name = "go_default_xtest",
    srcs = [
        "aes_gcm_content_cipher_test.go",
        "cipher_test.go",
        "decryption_client_test.go",
        "encryption_client_test.go",
        "mock_test.go",
        "strategy_test.go",
    ],
    importpath = "github.com/aws/aws-sdk-go/service/s3/s3crypto_test",
    deps = [
        ":go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/aws:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/aws/request:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/awstesting/unit:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/service/kms:go_default_library",
        "//vendor/github.com/aws/aws-sdk-go/service/s3:go_default_library",
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
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
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
