**The dataset has been moved to [HuggingFace](https://huggingface.co/Orange/rdfdial).**

# RDFDIAL dataset

This dataset provides dialogues annotated in dialogue acts and dialogue
state in and RDF based formalism.

There is a conversion of `sfxdial`, `dstc2` and `multiwoz2.3` datasets
as well as a few fully synthetic datasets.

Original dataset before conversion are available here:
- DSTC2: https://github.com/matthen/dstc
- Multiwoz 2.3: https://github.com/thu-coai/ConvLab-2/tree/master/data/multiwoz2.3
- SfxDial: https://www.repository.cam.ac.uk/items/62011578-23d4-4355-8878-5a150fb72b43

Each example follows this schema:
```
                {
                    dialogue_id: string,
                    turns: [
                        {
                            id: int8,
                            speaker: string,
                            text: string,
                            rdf-acts: [string],
                        }
                    ],
                    states: [
                        {
                            id: int8,
                            multi_relations: bool,
                            triples: [[string]],
                            turn_ids: [int8],
                        }
                    ],
                }
```


### Licenses

Converted datasets follow their original licenses:
- DSTC2: [GPL 3.0](https://github.com/matthen/dstc/blob/master/LICENSE)
- Multiwoz 2.3: [Apache 2.0](https://github.com/thu-coai/ConvLab-2/blob/master/LICENSE)
- SfxDial: [Attribution 2.0 UK: England & Wales](https://creativecommons.org/licenses/by/2.0/uk/)

Simulated conversation are provided with the following licenses:
- camrest-sim: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode)
- multiwoz-sim: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode)
