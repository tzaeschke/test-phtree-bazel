# Bazel bootstrapping

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive", "http_file")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

http_archive(
    name = "gtest",
#    build_file = "@third_party//gtest:BUILD",
    sha256 = "b4870bf121ff7795ba20d20bcdd8627b8e088f2d1dab299a031c1034eddc93d5",
    strip_prefix = "googletest-release-1.11.0",
    url = "https://github.com/google/googletest/archive/release-1.11.0.tar.gz",
)

http_archive(
    name = "absl",
    sha256 = "dcf71b9cba8dc0ca9940c4b316a0c796be8fab42b070bb6b7cab62b48f0e66c4",
    strip_prefix = "abseil-cpp-20211102.0",
    url = "https://github.com/abseil/abseil-cpp/archive/20211102.0.tar.gz",
)

#http_archive(
#    name = "phtree",
#    strip_prefix = "phtree-cpp-1.3.0",
#    url = "https://github.com/tzaeschke/phtree-cpp/tree/fix/75-enable-cmake-import-of-phtree",
#)

git_repository(
    name = "phtree",
    branch = "master",
#    commit = "8822dbd367eee7e3904d824b780b99009a4a9915",
    remote = "https://github.com/tzaeschke/phtree-cpp",
)

#local_repository(
#    name = "phtree",
#    path = "/home/xxxx/phtree-cpp",
#)
