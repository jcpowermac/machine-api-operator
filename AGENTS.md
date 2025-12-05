# AGENTS.md

## Build/Lint/Test Commands

- **Build**: `make build` or `make machine-api-operator`
- **Lint**: `make lint` or `golangci-lint run ./pkg/...`
- **Format**: `make fmt` or `gofmt -s -w`
- **Imports**: `make goimports` or `goimports -w`
- **Vet**: `make vet` or `go vet ./...`
- **Test**: `make test` or `./hack/ci-test.sh`
- **Single Test**: `go test -v ./pkg/webhooks/... -run TestValidateVSphereProviderSpec`

## Code Style Guidelines

- **Imports**: Use `goimports` to organize imports alphabetically with standard library first, then external packages
- **Formatting**: Follow `gofmt` standards with consistent indentation and spacing
- **Naming**: Use camelCase for variable names, PascalCase for exported functions/types
- **Types**: Prefer explicit type declarations over `var` when possible
- **Error Handling**: Handle errors explicitly with proper error wrapping and logging
- **Tests**: Use Ginkgo/Gomega for testing with comprehensive test cases covering all validation paths
- **Documentation**: Include godoc comments for exported functions and types

## Test Commands

- Run all tests: `make test`
- Run specific test suite: `go test -v ./pkg/webhooks/...`
- Run single test function: `go test -v ./pkg/webhooks/... -run TestValidateVSphereProviderSpec`
- Run with coverage: `go test -cover ./pkg/webhooks/...`