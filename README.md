# Terraria Server Images & Eggs
Terraria Server images and eggs for ARM (and x64) systems running Pterodactyl.

## How to use this?
### Usage outside of Pterodactyl
To use the image on your system, you can pull the image:\
`docker pull ghcr.io/alzhahir/terraria:main`

### Usage in Pterodactyl
If you want to use the image in Pterodactyl, just add the URL to your egg config:\
`ghcr.io/alzhahir/terraria:main`

#### In addition, an egg is also provided in this repository. You may navigate to the [egg folder](https://github.com/alzhahir/terraria/tree/main/egg) to download it, or [save this link](https://github.com/alzhahir/terraria/raw/main/egg/egg-terraria.json) as a JSON file.

## Note
The images provided should be compatible with `amd64` and `arm64` systems. However, `amd64` compatibility is untested. If you find any encounter using this image on amd64 systems, feel free to [contact me](https://www.alzhahir.com/contact) directly or [open an issue](https://github.com/alzhahir/terraria/issues) in this repository.
