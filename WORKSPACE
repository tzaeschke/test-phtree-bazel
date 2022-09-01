# Bazel bootstrapping

load("//tools/build_rules:http.bzl", "http_archive", "http_file")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

http_archive(
    name = "bazel_skylib",
    sha256 = "1dde365491125a3db70731e25658dfdd3bc5dbdfd11b840b3e987ecf043c7ca0",
    url = "https://github.com/bazelbuild/bazel-skylib/releases/download/0.9.0/bazel_skylib-0.9.0.tar.gz",
)

# NOTE: We make third_party/ its own bazel workspace because it allows to run `bazel build ...` without
# having all targets defined in third-party BUILD files in that directory buildable.
local_repository(
    name = "third_party",
    path = "third_party",
)

http_archive(
    name = "gtest",
    build_file = "@third_party//gtest:BUILD",
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
#    sha256 = "435e504f4a3587089f20f01962843ff4d7a94e0b30663067106109747f60cddc",
#    strip_prefix = "phtree-cpp-1.2.0",
#    url = "https://github.com/tzaeschke/phtree-cpp/archive/refs/tags/v1.2.0.tar.gz",
#)

#http_archive(
#    name = "phtree",
#    strip_prefix = "phtree-cpp-1.3.0",
#    url = "https://github.com/tzaeschke/phtree-cpp/tree/fix/75-enable-cmake-import-of-phtree",
#)

git_repository(
    name = "phtree",
    #branch = "fix/75-enable-cmake-import-of-phtree",
#    commit = "8822dbd367eee7e3904d824b780b99009a4a9915",
#    init_submodules, patch_args, patch_cmds, patch_cmds_win,
#               patch_tool, patches, recursive_init_submodules,
    remote = "https://github.com/tzaeschke/phtree-cpp",
               branch = "master",
)


#local_repository(
#    name = "phtree",
#    path = "/home/Franky/work/phtree-cpp-3",
#)
