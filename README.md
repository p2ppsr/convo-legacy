# Convo Mesenger

A private messaging app built with Project Babbage

[View it on the web](https://convo.babbage.systems)

## Overview

This is a React app demonstrating the use of [Babbage](https://projectbabbage.com) technologies with a simple private messaging experience.

- The app relies on the Babbage SDK to provide user accounts, key management and account recovery
- Bridgeport is used to provide a universal state machine backend powered by BSV transactions and real-time message and profile updates
- Hashbrown will soon provide a place to store picture messages and user profile photos

## A note on the (ab)use of redux

Some uses of Redux in this application are—shall we say—*unconventional*.

This is due primarily to a lack of sound Redux knowledge on the part of your author. However, I have done my best to ensure that these violations don't impact 
your ability to understand CWI and build your applications.

Try not to be too bothered by the occasional `store.dispatch` inside a React component. Pull requests that address these shortcomings are welcome :)

## License

The license for the code in this repository is the Open BSV License.


## October2026 Node build security maintenance

Build tooling uses Node22.23.4 with the retained frozen dependency lock and
historical peer resolution. Hosted PR CI verifies native Node/Brotli and the
retained source build with bounded registry requests. Application dependency
versions and browser contracts remain unchanged. Obsolete Cloud Run automation
is archived at `docs/legacy-cloud-run-deploy.yaml.txt` and cannot run. A successful
build does not establish application or production-restoration acceptance.
The retained Webpack4 compiler needs its legacy OpenSSL hash provider only in
the offline bundle-build step. This flag is not configured in a serving runtime.
