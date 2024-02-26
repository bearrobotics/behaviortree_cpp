load("@com_github_mvukov_rules_ros//ros:cc_defs.bzl", "cc_ros_library")

cc_ros_library(
    name = "behaviortree_cpp",
    srcs = glob(["src/**/*", "3rdparty/**/*.cpp"], exclude = ["src/example.cpp, shared_library_WIN.cpp"]) + 
    [
        "3rdparty/filesystem/fwd.h",
        "3rdparty/filesystem/path.h",
        "3rdparty/filesystem/resolver.h",

    ],
    hdrs = glob(["include/behaviortree_cpp_v3/**/*"]) + [
        "3rdparty/minitrace/minitrace.h"
    ],
    includes = [
        "include",
    ],
    tags = ["pennybot"],
    deps = [
        "@ros_comm//:roscpp_lib",
        "@boost//:coroutine",
        "@boost//:filesystem",
        "@cppzmq//:cppzmq",
    ],
)