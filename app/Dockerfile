FROM julia:latest@sha256:8cb392ab667d1961e12ec772d4854adcbf2bb16d5c4c8cd8438877b9d1c10e16
WORKDIR /app
COPY . .
RUN julia --project -e "using Pkg; Pkg.instantiate(); Pkg.precompile()"
ENTRYPOINT [ "julia", "--project", "src/app.jl" ]