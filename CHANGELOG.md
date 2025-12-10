# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0-alpha.2] - 2025-12-09

### Added
- **TypeScript Support**: Complete TypeScript type definitions for all components
- **Enhanced Testing**: Added comprehensive test cases covering edge cases and error handling
- **Documentation Examples**: Created detailed usage examples in `/examples` directory
  - `basic-usage.vue`: Basic ProTable implementation
  - `advanced-usage.vue`: Advanced features with custom slots and rendering
  - `cdn-usage.html`: CDN usage with live demo
- **CI/CD Pipeline**: GitHub Actions workflows for automated testing and publishing
  - `ci.yml`: Automated testing on push and pull requests
  - `publish.yml`: Automated publishing to npm and GitHub Packages
- **CDN Support**: UMD build now available via unpkg and jsDelivr
- **Package Renaming**: Changed from `vue3-pro-table` to `vue3-pro-table-antd` to avoid naming conflicts

### Fixed
- **TypeScript Generation**: Fixed vue-tsc compilation errors and type conflicts
- **Property Naming**: Standardized `hideInSearch` property (was `hideInForm`)
- **Form Validation**: Improved form validation handling in search component
- **Ref Exposure**: Fixed component ref exposure for better TypeScript support
- **Import Conflicts**: Removed duplicate `withDefaults` imports in Vue SFCs
- **Undefined Handling**: Improved handling of optional properties in templates

### Changed
- **Build Configuration**: Updated tsconfig.json for proper type generation
- **Package Structure**: Improved file organization and exports
- **Documentation**: Updated README with new package name and installation instructions
- **Version Bump**: Updated from 1.0.0-alpha.1 to 1.0.0-alpha.2

### Technical Details
- **Type Generation**: Now properly generates `.d.ts` files for all components
- **Test Coverage**: Added tests for request handling, pagination, form validation, and edge cases
- **Build Output**: Both UMD and ES module builds available
- **Dependencies**: Updated dev dependencies including vue-tsc to latest version

## [1.0.0-alpha.1] - 2025-12-09

### Initial Release
- **Core Components**: ProTable, ProTableSearch, ProTableTable, ProTableDefinition
- **Basic Features**:
  - Built-in search form with validation
  - Pagination support
  - Custom column configurations
  - Request function integration
  - Manual request mode
- **TypeScript**: Basic TypeScript support
- **Testing**: Initial test suite with basic component tests
- **Documentation**: README with basic usage examples
- **Build System**: Vite-based build with UMD and ES module outputs

[1.0.0-alpha.2]: https://github.com/saberviolet-M/vue3-pro-table/compare/v1.0.0-alpha.1...v1.0.0-alpha.2
[1.0.0-alpha.1]: https://github.com/saberviolet-M/vue3-pro-table/releases/tag/v1.0.0-alpha.1