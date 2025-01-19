# helm-charts

This is a work in progress, currently non-functional helm chart that we will be building on over time to have all the configuration parameters, values, and resources related to deploying the Openlane stack.

## TO-DO's

- Create / port helm buildkite plugin and git-commit buildkite plugin to allow for the automated tar ball + helm docs functionality
- Create basic automation to move the auto generated configuration map with all the Openlane environment variables into the chart https://github.com/theopenlane/core/blob/main/config/configmap.yaml
- Add the various configuration values / parameters for the core server into the `values.yaml`
- Add all the conditional wrappers / statements surrounding the template resources into the files so the `values.yaml` changes drive the resource changes
- Determine best approach for including a local PostgreSQL deployment alongside configuration values which would allow deploying the stack using a managed PG provider such as Neon
- Add additional chart dependencies for metrics, monitoring, logging
- Build / add anciallary k8s ecosystem services we'd want for our personal cluster deployment (e.g. external-dns, argoCD, cilium, cert-manager, etc.)