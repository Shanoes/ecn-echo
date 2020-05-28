
# Verify buildx installation and check platform support
docker buildx ls

# Create a new builder and select it
docker buildx create --name armbuilder
docker buildx use armbuilder 

# Bootstrap the build and verify
docker buildx inspect --bootstrap

# Build for AMD64 and ARMv7 platforms then tag and push to DockerHub
docker buildx build --platform linux/amd64,linux/arm/v7 -t shanoes/ecn-demo:latest --push .