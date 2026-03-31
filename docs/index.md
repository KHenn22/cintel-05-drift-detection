# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Your Files** - how to copy the example and create your version
- **Glossary** - project terms and concepts

## Additional Resources

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)

## Custom Project

### Dataset
System performance metrics including requests, errors, and latency
collected over a reference period and I current period, stored in CSV files.

### Signals
- Mean and median averages for requests, errors, and latency
- Absolute differences between reference and current periods
- Percentage change for each metric
- Boolean drift flags for both mean and median differences

### Experiments
- Median metrics added alongside means to test outlier sensitivity
- Percent change columns added to provide proportional context
  alongside absolute differences.  This allows for easier visualization of the substantial drift in error.
- Drift flags created for both mean and median metrics

### Results
All three metrics showed significant drift. Errors showed an increase of 173.9%,
requests 28.2%, and latency 47.9%. All 6 drift flags triggered
True for both mean and median metrics.

### Interpretation
The system is experiencing significant performance degradation across
all metrics. The close agreement between mean and median values confirms
the drift is real and not caused by outliers. The 174% increase in errors
is the most critical finding and would warrant immediate investigation
in a production environment.
