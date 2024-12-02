# QKDNetSim and NS-3 Configuration Guide

## Prerequisites
```bash
# Update system packages
sudo apt update
sudo apt upgrade

# Install required dependencies
sudo apt install build-essential cmake git python3-dev python3-pip
sudo pip3 install matplotlib
```

## NS-3 Configuration

### Clone Repository
```bash
# Clone qkdnetsim-v2 repository
git clone git@github.com:YOUR_USERNAME/qkdnetsim-v2.git
cd qkdnetsim-v2
```

### Configure .gitignore
```bash
# Create .gitignore file
touch .gitignore

# Add following entries to .gitignore
build/
cmake-cache/
*.lock
.lock-ns3_linux_build
```

### Build NS-3 with MPI Support
```bash
# Configure NS-3 with MPI
./ns3 configure --enable-mpi

# Build NS-3
./ns3 build
```

### Run Example
```bash
# Run a specific example (replace with your actual example)
./ns3 run qkdnetsim-example
```

## Additional Configuration

### Install Python Libraries
```bash
# Install additional Python libraries if needed
pip3 install numpy scipy
```

### Sync with Upstream Repository
```bash
# Add upstream remote
git remote add upstream git@github.com:QKDNetSim/qkdnetsim-v2.git

# Fetch upstream changes
git fetch upstream

# Sync your fork with upstream
git checkout main
git reset --hard upstream/main
git push origin main --force
```

## Troubleshooting
- Ensure all dependencies are installed
- Check MPI configuration
- Verify Python environment
- Confirm NS-3 build settings

## Best Practices
- Regularly update dependencies
- Use virtual environments
- Commit .gitignore early
- Keep track of configuration changes
