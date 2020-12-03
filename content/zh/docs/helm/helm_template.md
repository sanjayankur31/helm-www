---
title: "Helm 模板"
---

## helm template

本地渲染模板

### 简介

本地渲染模板并显示输出

通常在集群中查找或检索到的任何值都可以在本地伪造。另外，没有对chart有效性进行服务端测试。

```shell
helm template [NAME] [CHART] [flags]
```

### 可选项

```shell
  -a, --api-versions stringArray     Kubernetes api versions used for Capabilities.APIVersions
      --atomic                       if set, the installation process deletes the installation on failure. The --wait flag will be set automatically if --atomic is used
      --ca-file string               verify certificates of HTTPS-enabled servers using this CA bundle
      --cert-file string             identify HTTPS client using this SSL certificate file
      --create-namespace             create the release namespace if not present
      --dependency-update            run helm dependency update before installing the chart
      --description string           add a custom description
      --devel                        use development versions, too. Equivalent to version '>0.0.0-0'. If --version is set, this is ignored
      --disable-openapi-validation   if set, the installation process will not validate rendered templates against the Kubernetes OpenAPI Schema
      --dry-run                      simulate an install
  -g, --generate-name                generate the name (and omit the NAME parameter)
  -h, --help                         help for template
      --include-crds                 include CRDs in the templated output
      --insecure-skip-tls-verify     skip tls certificate checks for the chart download
      --is-upgrade                   set .Release.IsUpgrade instead of .Release.IsInstall
      --key-file string              identify HTTPS client using this SSL key file
      --keyring string               location of public keys used for verification (default "~/.gnupg/pubring.gpg")
      --name-template string         specify template used to name the release
      --no-hooks                     prevent hooks from running during install
      --output-dir string            writes the executed templates to files in output-dir instead of stdout
      --password string              chart repository password where to locate the requested chart
      --post-renderer postrenderer   the path to an executable to be used for post rendering. If it exists in $PATH, the binary will be used, otherwise it will try to look for the executable at the given path (default exec)
      --release-name                 use release name in the output-dir path.
      --render-subchart-notes        if set, render subchart notes along with the parent
      --replace                      re-use the given name, only if that name is a deleted release which remains in the history. This is unsafe in production
      --repo string                  chart repository url where to locate the requested chart
      --set stringArray              set values on the command line (can specify multiple or separate values with commas: key1=val1,key2=val2)
      --set-file stringArray         set values from respective files specified via the command line (can specify multiple or separate values with commas: key1=path1,key2=path2)
      --set-string stringArray       set STRING values on the command line (can specify multiple or separate values with commas: key1=val1,key2=val2)
  -s, --show-only stringArray        only show manifests rendered from the given templates
      --skip-crds                    if set, no CRDs will be installed. By default, CRDs are installed if not already present
      --timeout duration             time to wait for any individual Kubernetes operation (like Jobs for hooks) (default 5m0s)
      --username string              chart repository username where to locate the requested chart
      --validate                     validate your manifests against the Kubernetes cluster you are currently pointing at. This is the same validation performed on an install
  -f, --values strings               specify values in a YAML file or a URL (can specify multiple)
      --verify                       verify the package before using it
      --version string               specify the exact chart version to use. If this is not specified, the latest version is used
      --wait                         if set, will wait until all Pods, PVCs, Services, and minimum number of Pods of a Deployment, StatefulSet, or ReplicaSet are in a ready state before marking the release as successful. It will wait for as long as --timeout
```

### 从父命令继承的命令

```shell
      --debug                       enable verbose output
      --kube-apiserver string       the address and the port for the Kubernetes API server
      --kube-as-group stringArray   Group to impersonate for the operation, this flag can be repeated to specify multiple groups.
      --kube-as-user string         Username to impersonate for the operation
      --kube-context string         name of the kubeconfig context to use
      --kube-token string           bearer token used for authentication
      --kubeconfig string           path to the kubeconfig file
  -n, --namespace string            namespace scope for this request
      --registry-config string      path to the registry config file (default "~/.config/helm/registry.json")
      --repository-cache string     path to the file containing cached repository indexes (default "~/.cache/helm/repository")
      --repository-config string    path to the file containing repository names and URLs (default "~/.config/helm/repositories.yaml")
```

### 请参阅

* [helm](helm.md) - 针对Kubernetes的Helm包管理器