<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- GOAL -->
## Monitoring services

Pre-configured Helm charts to monitore your Kubernetes cluster and more.

### Built With

* [Helm](https://helm.sh)
* [Prometheus](https://prometheus.io)
* [Grafana](https://grafana.com)

<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

- A Kubernetes cluster
- `kubectl`
- `helm` on your local machine

### Installation

1. Clone the repo

   ```sh
   git clone git@github.com:rneuter/monitoring-helm-charts.git
   ```

2. Inspect [`values.yaml`](values.yaml) file and update ingress configuration for the Grafana chart

<!-- USAGE EXAMPLES -->
## Usage

```sh
# In a namespace, install or upgrade monitoring charts
helm upgrade $releaseName . -n $namespace --create-namespace -i
```

```sh
# In monitoring namespace, install or upgrade monitoring release with monitoring charts
helm upgrade monitoring . -n monitoring --create-namespace -i
```

Then you can visit the deployed Grafana following the host you set in [values.yaml](values.yaml).

_You should have set up a DNS record for your Grafana pointing to your cluster public IP, or something equivalent (e.g You can play with your `/etc/hosts`)._

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Best README Template](https://github.com/othneildrew/Best-README-Template)
* [Grafana Helm chart](https://github.com/grafana/helm-charts)
* [Prometheus Helm chart](https://github.com/prometheus-community/helm-charts)


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/rneuter/monitoring-helm-charts.svg?style=for-the-badge
[contributors-url]: https://github.com/rneuter/monitoring-helm-charts/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/rneuter/monitoring-helm-charts.svg?style=for-the-badge
[forks-url]: https://github.com/rneuter/monitoring-helm-charts/network/members
[stars-shield]: https://img.shields.io/github/stars/rneuter/monitoring-helm-charts.svg?style=for-the-badge
[stars-url]: https://github.com/rneuter/monitoring-helm-charts/stargazers
[issues-shield]: https://img.shields.io/github/issues/rneuter/monitoring-helm-charts.svg?style=for-the-badge
[issues-url]: https://github.com/rneuter/monitoring-helm-charts/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/rneuter
