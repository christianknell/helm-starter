# Helm Chart Starter

This repository contains starter templates for [Helm](https://helm.sh). Check out [the documentation](https://helm.sh/docs/topics/charts/#chart-starter-packs) to learn what starter templates are.

## Usage with [helm-starter](https://github.com/salesforce/helm-starter)

```bash
helm starter fetch https://github.com/christianknell/helm-starter.git
```

To use a starter, run:

```bash
helm create <CHART_NAME> --starter helm-starter/<STARTER_NAME>
```

For example to use the default starter template, run:

```bash
helm create <CHART_NAME> --starter helm-starter/default
```

## Needed changes after creation

After running the above command you still have to apply some changes to the created files.

1. `Chart.yaml`:
   1. change `appVersion`
   2. change `description`
   3. change `version`
   4. add `home`
   5. add `icon`
   6. add `maintainers`
   7. add `sources`
2. `values.yaml`:
   1. change `image.registry`
   2. change `image.repository`
   3. change `image.tag`
3. `README.md.gotmpl`:
   1. replace the helm registry host `christianknell https://christianknell.github.io/helm-charts`
   2. replace `<CHARTNAME>` with the real name of the chart
   3. add an `<INTRODUCTION>`
   4. replace `<APPLICATION_NAME>` and `<APPLICATION_LINK>` with the real values

That's basically all you have to do to have a clean starting point.
The provided `values.yaml` comes already with annotations for usage with [helm-docs](https://github.com/norwoodj/helm-docs).
See [these instructions](https://github.com/christianknell/helm-charts/tree/main/development) on how to create a `README.md` in an automatic fashion.

## Update with [helm-starter](https://github.com/salesforce/helm-starter)

```bash
helm starter update helm-starter
```
