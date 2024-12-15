# What's New?

## 1.1.0 - 2024-12-14

### Release highlights
- **New Search Filters**: Introduced distance-based and dietary preference filtering.
- **Enhanced Error Responses**: Updated error messages with detailed descriptions and suggestions.

### Added
- **Search Filters by Distance and Dietary Preferences**: Users can now filter donuts by proximity and dietary restrictions, such as gluten-free and vegan. [Commit 3f28a6c](https://www.github.com) [@contributor1](https://www.github.com/contributor1)
- **Error Messages with Debugging Suggestions**: Added a `resolution_suggestions` field to error responses for easier troubleshooting. [Commit 59d34a7](https://www.github.com) [@contributor4](https://www.github.com/contributor4)

### Changed
- **Default Timeout**: Reduced API default timeout duration from 30 seconds to 15 seconds to improve failover response times. [Commit 4ac72f1](https://www.github.com) [@contributor5](https://www.github.com/contributor5)

### Fixed
- **Pagination Issues**: Resolved an issue where pagination parameters were ignored for specific queries. [Commit d73a5b1](https://www.github.com) [@contributor7](https://www.github.com/contributor7)

### Security
- **Input Validation Improvements**: Enhanced input validation to mitigate risks like SQL injection. [Commit c83d7f1](https://www.github.com) [@contributor10](https://www.github.com/contributor10)

