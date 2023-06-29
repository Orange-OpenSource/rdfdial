# RDFDIAL dataset

This dataset provides dialogues annotated in dialogue acts and dialogue
state in and RDF based formalism.

There is a conversion of `sfxdial`, `dstc2` and `multiwoz-convlab2.3` datasets
as well as a few fully synthetic datasets.

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

