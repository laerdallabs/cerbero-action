# Cerbero Action (for GStreamer)

This GitHub action facilitates configuring a workflow with a specific installation of GStreamer.  If a specific version is not found ready to download, this action will also attempt to build GStreamer using the provided configuration arguments.  Once GStreamer is either downloaded or built, it is installed and the OS environment configured for its use.

> NOTE: this has currently been tested on Windows runners; Linux support is not fully supported at this time.

## Usage

```yaml
- uses: laerdallabs/cerbero-action@main
  with:
    cerbero-repo:
      # Repository to use for Cerbero
      # required: false
      # default: https://gitlab.freedesktop.org/gstreamer/cerbero.git
    cerbero-ref:
      # description: 'Ref to use for Cerbero'
      # required: false
      # default: main
    config:
      # description: 'Name of the configuration file to use'
      # required: false
    cerbero-args:
      # description: 'Additional args to pass to Cerbero'
      # required: false
      # default: '--clocktime --timestamps'
    cerbero-package-args:
      # description: 'Additional args to pass to Cerbero package'
      # required: false
      # default: ''
    cleanup:
      # description: 'Whether to clean the Cerbero build directory'
      # required: false
      # default: 'true'
    no-cache:
      # description: 'Whether to disable restoring from cache'
      # required: false
      # default: 'false'
    s3-download-paths:
      # description: 'S3 paths to download from'
      # required: false
    s3-upload-path:
      # description: 'S3 path to upload to'
      # required: false
    gst-plugins-rs-repo:
      # description: 'Repository to use for gst-plugins-rs'
      # required: false
    gst-plugins-rs-ref:
      # description: 'Ref/tag to use for gst-plugins-rs'
      # required: false
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).
