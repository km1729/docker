Build an image
```bash
docker build -t asl .
```

Run a container
```bash
docker run -it --name asl asl
```

recommended dependencies
conda install -c conda-forge xarray dask netCDF4 bottleneck
