licenses(["notice"]) 
load("@rules_foreign_cc//foreign_cc:defs.bzl", "cmake")
filegroup(
    name = "all",
    srcs =  glob(["**"])
)
cmake(
    name = "behaviortree_cpp",
    cache_entries = {
        "BTCPP_UNIT_TESTS": "OFF",
    },
    lib_source = ":all",
    out_shared_libs = select({
        "//conditions:default": ["libbehaviortree_cpp.so"],
    }),
    visibility = [
        "//visibility:public"
    ],
)