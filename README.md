# Veracode SBOM

## Generate SBOM with Veracode CLI
```sh
# generates sbom for directory source at <path> to stdout
veracode sbom --type directory --source <path>

# generates sbom for current directory source at the below url in cyclonedx output file
veracode sbom --type directory --source . -o verademo-java.bom.json -f cyclonedx-json

# generates sbom for repo source at the below url in json output file
veracode sbom --type repo --source <repo> -o <file>
veracode sbom --type repo --source https://github.com/wsandersvc/verademo -o <file>

# generates sbom for repo source at the below url in cyclonedx output file
veracode sbom --type repo --source https://github.com/wsandersvc/verademo -o verademo-java.bom.json -f cyclonedx-json
```

## Generate SBOM with SCA-agent (srcclr)
```sh
srcclr scan . --sbom cyclonedx1.6+json --output verademo-java.bom.json
srcclr scan . --sbom spdx2.3+json --output verademo-java.bom.json   
```

## Scan SBOM with SCA-agent (srcclr)
```sh
srcclr scan . --quick --scan-collectors SbomQuickScanCollector
```