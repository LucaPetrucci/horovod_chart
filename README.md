# Helm Charts for PLAS 

In this repository you can find all the Helm charts used by the [PLAS project](https://github.com/PlatformedTasks/Documentation).

PLAS is a project funded by the [GÉANT Innovation Programme](https://community.geant.org/community-programme-portfolio/innovation-programme/) initiative to extend the [GÉANT Cloud Flow (GCF)](https://clouds.geant.org/community-cloud/) to be capable of performing platformed-tasks in the cloud.

## Requirements
* Kubernetes 1.21+
* Helm 3.2+

## Usage
```
$ helm repo add plas https://platformedtasks.github.io/PLAS-charts/charts
$ helm repo update
$ helm search repo plas
$ helm install my-release plas/<chart>
```

---

Switch to the `gh-pages` branch to see all the charts.


## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  helm repo add <alias> https://<orgname>.github.io/helm-charts

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
<alias>` to see the charts.

To install the <chart-name> chart:

    helm install my-<chart-name> <alias>/<chart-name>

To uninstall the chart:

    helm delete my-<chart-name>
---
# README

This command packages a chart into a versioned chart archive file. If a path is given, this will look at that path for a chart (which must contain a Chart.yaml file) and then package that directory.

Versioned chart archives are used by Helm package repositories.

```
helm package charts/horovod --destination=charts/ --version=XYZ
helm package charts/spark --destination=charts
```

Read the current directory and generate an index file based on the charts found.

This tool is used for creating an 'index.yaml' file for a chart repository. To set an absolute URL to the charts, use '--url' flag.

```
helm repo index charts
```

> **Remember:** use git to update this repo
