# Change log
<!-- Template:
## [version] — YYYY-MM-DD

### Security
### Added
### Changed
### Deprecated
### Removed
### Fixed
-->

## [0.2.2] — 2024-12-23

### Security
### Added
1. Created new methods, `update_refined_values` and `refine_iteration` to provide an alternate interface to iteratively call the refinement function and update the values.  
2. Created new methods `update_values` and `update_values_parallel` to provide an easier way to update the base grid values. 
### Changed
Reduced memory overhead of `GridIteratorWithCache` by 2x. This also appears to improve performance by 10-20%. This is a breaking change for serializing/deserializing a `LinearGrid`.
### Deprecated
### Removed
### Fixed

## [0.2.1] — 2024-12-20

### Security
### Added
Created a new `refine_parallel` method for the `SparseGrid` trait. The results in values being filled for the refined nodes in parallel.
### Changed
`RefinementFunctor` must now implement Send + Sync.
### Deprecated
### Removed
Removed the useless sorting in the `refine` function. Presently we do not limit the number of nodes to refine in a given iteration.
### Fixed

## [0.2.0] — 2024-12-16

### Security
### Added
### Changed
Improved performance of `CombinationGrid` interpolation by ~40%. It is now on par with the performance of TASMANIAN.
### Deprecated
### Removed
### Fixed

## [0.1.1] — 2024-12-14

### Security
### Added
### Changed
### Deprecated
### Removed
Removed unused tests file.
### Fixed

## [0.1.0] — 2024-12-14

### Security
### Added
Initial commit of base capabilities
### Changed
### Deprecated
### Removed
### Fixed