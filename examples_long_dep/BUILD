package(default_visibility = ["//visibility:private"])

cc_binary(
    name = "example_new",
    srcs = ["example.cc"],
    visibility = [
        "//visibility:public",
    ],
    deps = [
        "@absl//absl/container:flat_hash_set",
        "@phtree//phtree:phtree",
    ],
)
