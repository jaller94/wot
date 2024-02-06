# TD and Bindings

Summary of main points from the discussion.

## [Sept 14, TD and Bindings](https://www.w3.org/2023/09/14-wot-minutes.html#t04)

### Intro from Sebastian
- [Slides](https://github.com/w3c/wot/blob/main/PRESENTATIONS/2023-09-tpac/2023-09-14-TD2-Planning-Sebastian.pdf)
- Plan to reorganize and combine documents
     - Incorporate the Binding Templates document into the TD document
     - Expand the separate binding documents to include security schemes
     - Allow the separate binding documents to be managed by external organizations that control the protocols
     - The TD spec will only describe the mechanism of binding
     - Separate discussion on the topic of a registry
     - Integrators might implement just what they need - BACnet example
     - 2-step approach, first what information is needed, then think about how later
- Other topics in TD reorganization
     - base terms
     - common server connection 
     - extensions to protocols - Modbus endian-ness example
     - driver parameters - BACnet example
     - reduce duplication of text - content type example
- Manageable actions 
     - BACnet has return codes, non-specific to BACnet 
     - there should be an abstract interaction model and concrete subprotocol 
     - TD doesn't model protocols in detail
     - we could try to describe the existing mechanisms and create the abstraction from those
     - there should be a default mechanism to drive eventual standardization
     - there are other long-running affordance patterns like chained alarm events
     - TD is a static descriptor and manageable actions require dynamic interaction
     - state charts may be a solution 
     - we need to clarify the needs
     - there could be a change from the static model
     - process of developing runtime interworking between different patterns to lead to a minimum set that others can build on - BACnet example
     - "temporal actions" related topic
     - Canonicalization of TD documents - required for cryptographic signatures
     - Time series data
     - TD Linting - opinioned format 
     - Custom implementations
     - Semantic support 
     - Backward compatibility
 
### Binding Registry
- ([Slides](https://github.com/w3c/wot/blob/main/PRESENTATIONS/2023-09-tpac/2023-09-14-WoT-TPAC-Registry-Korkan.pdf))
     - The binding mechanism will be described in the TD spec
     - accommodate more diverse protocols
     - flexibility is required, a REC document can't be changed
     - the REC document can include a registry table which can be updated through a special process https://www.w3.org/2023/Process-20230612/
     - we would define the rules for adding to the table
     - W3C WebCodecs example https://www.w3.org/TR/webcodecs-codec-registry/
     - IANA is another example
     - Need to have a follow-up discussion with WebCodecs (action?)
     - What are the requirements and guarantees
     - 2-step approach - first, what kind of information is needed, then how the registry will work
     - more examples of different registries
     - https://github.com/w3c/tt-profile-registry/pulse
     - https://www.w3.org/TR/ttml-profile-registry/
     - https://www.w3.org/TR/mse-byte-stream-format-registry/
     - https://www.w3.org/TR/webcodecs-codec-registry/
     - https://www.w3.org/TR/did-spec-registries/
- Discussion:
     - Changes in the main document may require changing documents in all of the registered bindings - a potential issue
     - how do we remove entries
     - TD version tracking
     - registered bindings should be immutable
     - there should be a validation step for bindings
     - The rule for publishing all "intermediate" TDs versions should also apply to bindings to avoid "skips" preventing upgrades
