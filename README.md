# README

This command packages a chart into a versioned chart archive file. If a path is given, this will look at that path for a chart (which must contain a Chart.yaml file) and then package that directory.

Versioned chart archives are used by Helm package repositories.

```
helm package charts/horovod --destination=charts/ --version=XYZ
```

Read the current directory and generate an index file based on the charts found.

This tool is used for creating an 'index.yaml' file for a chart repository. To set an absolute URL to the charts, use '--url' flag.

```
helm repo index charts
```

> **Remember:** use git to update this repo
