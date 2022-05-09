# dafka-producer-helm-chart

This is a Helm Chart for the awesome [dafka-producer](https://github.com/osskit/dafka-producer) project.

## Usage

[Helm](https://helm.sh) must be installed to use the charts. Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add dafka-producer https://osskit.github.io/dafka-producer-helm-chart

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages. You can then run `helm search repo dafka-producer` to see the charts.

To install the dafka-producer chart:

    helm upgrade my-dafka-producer dafka-producer/dafka-producer --install --namespace data --create-namespace

To uninstall the chart:

    helm delete my-dafka-producer --namespace data

## Configuration

To get an overview of the configurable and default Values check out the Chart specific [README](./charts/dafka-producer/README.md).
