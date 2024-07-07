This [Code Ocean](https://codeocean.com) Compute Capsule will allow you to run and reproduce the results of [Previous Capsule - acme-2.22.0 - Original](https://acmecorp-edge.codeocean.com/capsule/5642822/tree) on your local machine<sup>1</sup>. Follow the instructions below, or consult [our knowledge base](https://docs.codeocean.com/user-guide/compute-capsule-basics/managing-capsules/exporting-capsules-to-your-local-machine) for more information. Don't hesitate to reach out to [Support](mailto:support@codeocean.com) if you have any questions.

<sup>1</sup> You may need access to additional hardware and/or software licenses.

# Prerequisites

- [Docker Community Edition (CE)](https://www.docker.com/community-edition)

# Instructions

## Download attached Data Assets

In order to fetch the Data Asset(s) this Capsule depends on, download them into the Capsule's `data` folder:
* [Bernie](https://acmecorp-edge.codeocean.com/data-assets/4a117340-fb77-4f8c-b4d9-81e613abe125) should be downloaded to `data/Test`

## Log in to the Docker registry

In your terminal, execute the following command, providing your password or API key when prompted for it:
```shell
docker login -u eden.berman@codeocean.com registry.acmecorp-edge.codeocean.com
```

## Run the Capsule to reproduce the results

In your terminal, navigate to the folder where you've extracted the Capsule and execute the following command, adjusting parameters as needed:
```shell
docker run --platform linux/amd64 --rm \
  --workdir /code \
  --volume "$PWD/code":/code \
  --volume "$PWD/data":/data \
  --volume "$PWD/results":/results \
  registry.acmecorp-edge.codeocean.com/capsule/0d95320f-2253-4e1a-8101-aa8860d45e6f \
  bash run a
```
