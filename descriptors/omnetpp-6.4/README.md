# Model Descriptors for OMNeT++ 6.4

This folder contains project descriptors for the IDE's "Install Simulation Models"
dialog, for the OMNeT++ 6.4 release.

## Principles

- **Small, curated set of models.** We include only a handful of models (5..10)
  so that we interactively test-install every single entry before a release.
  This is not meant to be a comprehensive model catalog.

- **Fixed dependencies.** Every model should depend on one specific version
  of INET. It should NOT be supported to support this-and-that version of INET.

- **Simple build configurations only.** Descriptors should cover the most
  straightforward setups. Users with more complex needs (optional libs like z3,
  emulation, support for 3rd party model integration, etc) should use `opp_env` instead.

## Testing Locally

Set the environment variable before launching the IDE:

    export OMNETPP_IDE_INSTALL_MODELS_DESCRIPTORS_DIR=/path/to/this/directory

The dialog will load descriptors from this local directory instead of the server.
