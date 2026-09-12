# Maximum Task Size Rule

Split an issue whenever any of the following is true:
- it produces more than one independently reviewable artifact;
- it has more than one independent acceptance outcome;
- one part can fail QA while another can pass;
- it spans research + modelling + specification + QA;
- it mixes multiple business capabilities;
- it requires different source/evidence sets;
- it contains separate happy-path and complex exception modelling that can be verified independently.

A valid work issue should normally be completable and QA-verifiable as one coherent change.
