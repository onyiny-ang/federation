load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "date.go",
        "time.go",
        "timerfc1123.go",
        "unixtime.go",
        "utility.go",
    ],
    importpath = "github.com/Azure/go-autorest/autorest/date",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = [
        "date_test.go",
        "time_test.go",
        "timerfc1123_test.go",
        "unixtime_test.go",
    ],
    importpath = "github.com/Azure/go-autorest/autorest/date",
    library = ":go_default_library",
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
