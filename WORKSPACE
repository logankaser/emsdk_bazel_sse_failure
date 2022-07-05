load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Emscripten
http_archive(
    name = "emsdk",
    strip_prefix = "emsdk-3.1.15/bazel",
    url = "https://github.com/emscripten-core/emsdk/archive/refs/tags/3.1.15.tar.gz",
    sha256 = "74c7c54b3544555ec38d1e9dcc7e90b9f49ed0e04f2cc3fd44663c598af24124",
)
load("@emsdk//:deps.bzl", emsdk_deps = "deps")
emsdk_deps()
load("@emsdk//:emscripten_deps.bzl", emsdk_emscripten_deps = "emscripten_deps")
# Default to latest version available in the archive
emsdk_emscripten_deps()
