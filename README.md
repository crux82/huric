# <u>Hu</u>man <u>R</u>obot <u>I</u>nteraction <u>C</u>orpus (HuRIC 2.0)

HuRIC (<u>Hu</u>man <u>R</u>obot <u>I</u>nteraction <u>C</u>orpus) is a resource that has been gathered  as a collaboration between the [Semantic Analytics Group (SAG)](http://sag.art.uniroma2.it) from the University of Roma, Tor Vergata, and the [Laboratory of Cognitive Cooperating Robots (Lab.Ro.Co.Co.)](http://labrococo.dis.uniroma1.it/) at Sapienza, University of Rome. The basic idea of this project is to build a corpus for Human Robot Interaction in Natural Language containing information that are yet oriented to a specific application domain, e.g. the house service robotics, but at the same time inspired by sound linguistic theories, that are by definition decoupled from such a domain.

HuRIC is designed to enable the **Grounded Language Interpretation** of robotic commands, i.e., make the interpretation process of a robotic command dependent from the specific environment where the utterance is expressed.  Without any contestual information, a command such as *"take the mug next to the keyboard"* is ambiguous: it may in fact express the need of *picking up the mug that is near the keyboard* or to *bring the mug whose position is not expressed toward a new position near the keyboard*. Whithout knowing the actual placement of the ``mug`` and the ``keyboard``in the environment, it is not possible to decide the suitable interpretation, i.e. correctly assign the intended meaning to the command.


HuRIC is based on the theory of [Frame Semantics](https://framenet.icsi.berkeley.edu/fndrupal/) and captures cognitive information about the real-world situations and events expressed in sentences. The most interesting feature is that HuRIC is not system or robot dependent and these regards the type of accepted sentences and the adopted formalism for representing and extracting their interpretation. 

In order to enable the learning of Grounded Language Interpretation processes, each command in HuRIC is paired with a Semantic Map, reflecting the naming and disposition of entities in the environment that are referred by the interpretation. 

HuRIC is released as an open source resource, under the Apache 2.0 license.



## Corpus Definition


HuRIC exploits different situations representing possible commands given to a robot in a house environment. The corpus is composed of different subsets, characterized by different order of complexity and designed to differently stress the language recognition architecture.
Each sentence is annotated linguistically as well as conceptually. In linguistic terms lemmas, POS tags, dependency trees, and Frame Semantics are annotated over the sentence. Semantic frames and frame elements are associated to sentence fragments (e.g. verbs and their syntactic arguments) and correspoind to the adopted meaning representation formalisms for the underlying command: they also conceptually reflect the actions requested to a robot, that are usually the actions it can carry out in a home environment.

HuRIC provides commands in **two different languages**: English and Italian. While the English subset contains 656 sentences, 241 commands are available in Italian. Almost all Italian sentences are translations of the original commands in English and the corpus keeps an alignment between them. 

The number of annotated sentences, number of frames, and further statistics are reported in Table 1.

<center>

| | **English** | **Italian** |
--- | --- | ---
| *Number of examples* | 656 | 241 |
| *Number of frames* | 18 | 14 |
| *Number of predicates* | 762 | 272 |
| *Number of roles* | 34 | 28 |
| *Predicates per sentence* | 1.16 | 1.13 |
| *Sentences per frame* | 36.44 | 17.21 |
| *Roles per sentence* | 2.02 | 1.90 |
| *Entities per sentence* | 6.59 | 6.97 |
Table 1: HuRIC: some statistics

</center>

Detailed statistics about the number of sentences for each frame and frame elements are reported in Table 2 and Table 3 for the English and Italian subsets, respectively.

<center>

| Frame | Ex | Frame | Ex | Frame | Ex |
| --- | ---: | --- | ---: | --- | ---: |
| **Motion** | 143 | **Bringing** | 153 | **Cotheme** | 39 |
| <span style="font-variant:small-caps;">Goal</span> | 129 | <span style="font-variant:small-caps;">Theme</span> | 153 | <span style="font-variant:small-caps;">Cotheme</span> | 39
 <span style="font-variant:small-caps;">Theme</span> | 23 | <span style="font-variant:small-caps;">Goal</span> | 95 | <span style="font-variant:small-caps;">Manner</span> | 9
 <span style="font-variant:small-caps;">Direction</span> | 9 | <span style="font-variant:small-caps;">Beneficiary</span> | 56 | <span style="font-variant:small-caps;">Goal</span> | 8
 <span style="font-variant:small-caps;">Path</span> | 9 | <span style="font-variant:small-caps;">Agent</span> | 39 | <span style="font-variant:small-caps;">Theme</span> | 4
 <span style="font-variant:small-caps;">Manner</span> | 4 | <span style="font-variant:small-caps;">Source</span> | 18 | <span style="font-variant:small-caps;">Speed</span> | 1
 <span style="font-variant:small-caps;">Area</span> | 2 | <span style="font-variant:small-caps;">Manner</span> | 1 | <span style="font-variant:small-caps;">Path</span> | 1
 <span style="font-variant:small-caps;">Distance</span> | 1 | <span style="font-variant:small-caps;">Area</span> | 1 | <span style="font-variant:small-caps;">Area</span> | 1
 <span style="font-variant:small-caps;">Source</span> | 1 | 
| **Locating** | 90 | **Inspecting** | 29 | **Taking** | 80
 <span style="font-variant:small-caps;">Phenomenon</span> | 89 | <span style="font-variant:small-caps;">Ground</span> | 28 | <span style="font-variant:small-caps;">Theme</span> | 80
 <span style="font-variant:small-caps;">Ground</span> | 34 | <span style="font-variant:small-caps;">Desired_state</span> | 9 | <span style="font-variant:small-caps;">Source</span> | 16
 <span style="font-variant:small-caps;">Cognizer</span> | 10 | <span style="font-variant:small-caps;">Inspector</span> | 5 | <span style="font-variant:small-caps;">Agent</span> | 8
 <span style="font-variant:small-caps;">Purpose</span> | 5 | <span style="font-variant:small-caps;">Unwanted_entity</span> | 2 | <span style="font-variant:small-caps;">Purpose</span> | 2
 <span style="font-variant:small-caps;">Manner</span> | 2 | 
 **Change\_direction** | 11 | **Arriving** | 12 | **Giving** | 10
 <span style="font-variant:small-caps;">Direction</span> | 11 | <span style="font-variant:small-caps;">Goal</span> | 11 | <span style="font-variant:small-caps;">Recipient</span> | 10
 <span style="font-variant:small-caps;">Angle</span> | 3 | <span style="font-variant:small-caps;">Path</span> | 5 | <span style="font-variant:small-caps;">Theme</span> | 10
 <span style="font-variant:small-caps;">Theme</span> | 1 | <span style="font-variant:small-caps;">Manner</span> | 1 | <span style="font-variant:small-caps;">Donor</span> | 4
 <span style="font-variant:small-caps;">Speed</span> | 1 | <span style="font-variant:small-caps;">Theme</span> | 1 | <span style="font-variant:small-caps;">Reason</span> | 1
 **Placing** | 52 | **Closure** | 19 | **Change\_operational\_state** | 49
 <span style="font-variant:small-caps;">Theme</span> | 52 | <span style="font-variant:small-caps;">Containing_object</span> | 11 | <span style="font-variant:small-caps;">Device</span> | 49
 <span style="font-variant:small-caps;">Goal</span> | 51 | <span style="font-variant:small-caps;">Container_portal</span> | 8 | <span style="font-variant:small-caps;">Operational_state</span> | 43
 <span style="font-variant:small-caps;">Agent</span> | 7 | <span style="font-variant:small-caps;">Agent</span> | 7 | <span style="font-variant:small-caps;">Agent</span> | 17
 <span style="font-variant:small-caps;">Area</span> | 1 | <span style="font-variant:small-caps;">Degree</span> | 2 | 
 **Being\_located** | 38 | **Attaching** | 11 | **Releasing** | 9
 <span style="font-variant:small-caps;">Theme</span> | 38 | <span style="font-variant:small-caps;">Goal</span> | 11 | <span style="font-variant:small-caps;">Theme</span> | 9
 <span style="font-variant:small-caps;">Location</span> | 34 | <span style="font-variant:small-caps;">Item</span> | 6 | <span style="font-variant:small-caps;">Goal</span> | 5
 <span style="font-variant:small-caps;">Place</span> | 1 | <span style="font-variant:small-caps;">Items</span> | 1 | 
 **Perception\_active** | 6 | **Being\_in\_category** | 11 | **Manipulation** | 5
 <span style="font-variant:small-caps;">Phenomenon</span> | 6 | <span style="font-variant:small-caps;">Item</span> | 11 | <span style="font-variant:small-caps;">Entity</span> | 5
 <span style="font-variant:small-caps;">Manner</span> | 1 | <span style="font-variant:small-caps;">Category</span> | 11 | 

Table 2: Distribution of frames and frame elements in the English dataset

</center>

<center>

| Frame | Ex | Frame | Ex | Frame | Ex |
| --- | ---: | --- | ---: | --- | ---: |
| **Motion** | <span>51</span> | **Locating** | <span>27</span> | **Inspecting** | <span>4</span> |
| <span style="font-variant:small-caps;">Goal</span> | <span>28</span> | <span style="font-variant:small-caps;">Phenomenon</span> | <span>27</span> | <span style="font-variant:small-caps;">Ground</span> | <span>2</span> |
| <span style="font-variant:small-caps;">Direction</span> | <span>20</span> | <span style="font-variant:small-caps;">Ground</span> | <span>6</span> | <span style="font-variant:small-caps;">Unwanted_entity</span> | <span>2</span> |
| <span style="font-variant:small-caps;">Distance</span> | <span>13</span> | <span style="font-variant:small-caps;">Manner</span> | <span>2</span> | <span style="font-variant:small-caps;">Desired_state</span> | <span>2</span> |
| <span style="font-variant:small-caps;">Speed</span> | <span>8</span> | <span style="font-variant:small-caps;">Purpose</span> | <span>1</span> | <span style="font-variant:small-caps;">Instrument</span> | <span>1</span> |
| <span style="font-variant:small-caps;">Theme</span> | <span>3</span> 
| <span style="font-variant:small-caps;">Path</span> | <span>2</span> 
| <span style="font-variant:small-caps;">Manner</span> | <span>1</span> 
| <span style="font-variant:small-caps;">Source</span> | <span>1</span> |
 **Bringing** | <span>59</span> | **Cotheme** | <span>13</span> | **Placing** | <span>18</span> |
| <span style="font-variant:small-caps;">Theme</span> | <span>60</span> | <span style="font-variant:small-caps;">Cotheme</span> | <span>13</span> | <span style="font-variant:small-caps;">Theme</span> | <span>18</span> |
| <span style="font-variant:small-caps;">Beneficiary</span> | <span>31</span> | <span style="font-variant:small-caps;">Manner</span> | <span>6</span> | <span style="font-variant:small-caps;">Goal</span> | <span>17</span> |
| <span style="font-variant:small-caps;">Goal</span> | <span>26</span> | <span style="font-variant:small-caps;">Goal</span> | <span>5</span> | <span style="font-variant:small-caps;">Area</span> | <span>1</span> |
| <span style="font-variant:small-caps;">Source</span> | <span>8</span> 
 **Closure** | <span>10</span> | **Giving** | <span>7</span> | **Change\_direction** | <span>21</span> |
| <span style="font-variant:small-caps;">Container_portal</span> | <span>6</span> | <span style="font-variant:small-caps;">Theme</span> | <span>7</span> | <span style="font-variant:small-caps;">Direction</span> | <span>21</span> |
| <span style="font-variant:small-caps;">Containing_object</span> | <span>5</span> | <span style="font-variant:small-caps;">Recipient</span> | <span>6</span> | <span style="font-variant:small-caps;">Angle</span> | <span>9</span> |
| <span style="font-variant:small-caps;">Degree</span> | <span>1</span> | <span style="font-variant:small-caps;">Donor</span> | <span>1</span> | <span style="font-variant:small-caps;">Speed</span> | <span>9</span>
 **Taking** | <span>22</span> | **Being\_located** | <span>14</span> | **Being\_in\_category** | <span>4</span> |
| <span style="font-variant:small-caps;">Theme</span> | <span>22</span> | <span style="font-variant:small-caps;">Location</span> | <span>14</span> | <span style="font-variant:small-caps;">Item</span> | <span>4</span> |
| <span style="font-variant:small-caps;">Source</span> | <span>8</span> | <span style="font-variant:small-caps;">Theme</span> | <span>12</span> | <span style="font-variant:small-caps;">Category</span> | <span>4</span>
 **Releasing** | <span>8</span> | **Change\_operational\_state** | <span>14</span> 
 <span style="font-variant:small-caps;">Theme</span> | <span>8</span> | <span style="font-variant:small-caps;">Device</span> | <span>14</span> 
 <span style="font-variant:small-caps;">Place</span> | <span>3</span>  

Table 3: Distribution of frames and frame elements in the Italian dataset

</center>


### Corpus Release

This repository contains the whole HuRIC corpus, a collection of robotics commands.

It is composed of 2 versions, one for each language:

* `en`: the English version of HuRIC
* `it`: the Italian verison of HuRIC

The English version is further decomposed in 7 subsets, characterized by different order of complexity and designed to differently stress a labeling architecture.

#### Release format

The current release of HuRIC is made available through an XML-based format, whose extension is `.hrc`. An example is provided below.
The targeted command is *"take the mug next to the keyboard"*

```html
<?xml version="1.0" encoding="UTF-8"?>
<huricExample id="2650">
  <commands>
    <command>
      <sentence>take the mug next to the keyboard</sentence>
      <tokens>
        <token id="1" lemma="take" pos="VB" surface="take" />
        <token id="2" lemma="the" pos="DT" surface="the" />
        <token id="3" lemma="mug" pos="NN" surface="mug" />
        <token id="4" lemma="next" pos="JJ" surface="next" />
        <token id="5" lemma="to" pos="TO" surface="to" />
        <token id="6" lemma="the" pos="DT" surface="the" />
        <token id="7" lemma="keyboard" pos="NN" surface="keyboard" />
      </tokens>
      <dependencies>
        <dep from="0" to="1" type="root" />
        <dep from="1" to="3" type="dobj" />
        <dep from="3" to="2" type="det" />
        <dep from="1" to="4" type="advmod" />
        <dep from="4" to="7" type="nmod" />
        <dep from="7" to="5" type="case" />
        <dep from="7" to="6" type="det" />
      </dependencies>
      <semantics>
        <frames>
          <frame name="Bringing">
            <lexicalUnit>
              <token id="1" />
            </lexicalUnit>
            <frameElements>
              <frameElement>
                <type name="Theme" />
                <span startId="2" endId="3" />
              </frameElement>
              <frameElement>
                <type name="Goal" />
                <span startId="4" endId="7" />
              </frameElement>
            </frameElements>
          </frame>
        </frames>
      </semantics>
    </command>
  </commands>
  <semanticMap>
    <entities>
      <entity atom="p1" type="Cup">
        <attributes>
          <attribute name="contain_ability">
            <value>true</value>
          </attribute>
          <attribute name="preferred_lexical_reference">
            <value>cup</value>
          </attribute>
          <attribute name="lexical_references">
            <value>cup</value>
            <value>mug</value>
            <value>coffee cup</value>
            <value>bowl</value>
          </attribute>
        </attributes>
        <coordinate angle="0.0" x="2.0" y="5.0" z="0.0" />
      </entity>
      ...
      <entity atom="k1" type="Keyboard">
        <attributes>
          <attribute name="contain_ability">
            <value>false</value>
          </attribute>
          <attribute name="lexical_references">
            <value>keyboard</value>
            <value>console</value>
          </attribute>
        </attributes>
        <coordinate angle="0.0" x="4.0" y="1.0" z="0.0" />
      </entity>
    </entities>
  </semanticMap>
  <lexicalGroundings>
    <lexicalGrounding atom="p1" tokenId="3" />
    <lexicalGrounding atom="k1" tokenId="7" />
  </lexicalGroundings>
</huricExample>
```

Hence, for each command, the following information are provided:

1. the whole sentence (i.e., `<sentence/>` tag), like the command above `take the mug next to the keyboard`.
2. the list of tokens composing the command, along with the corresponding lemma and POS tags (i.e., the `<tokens/>` XML tag)
	* notice that each `token` is referred with an `id`which is used in the rest of the file to refer to it. 
3. the syntactic information, in terms of dependency relations among tokens (i.e., the `<dependencies/>` tag)
	* in the example above a row like `<dep from="1" to="3" type="dobj" />` means that the third word referred by `<token id="3" lemma="mug" pos="NN" surface="mug" />` expresses the direct object (i.e., the `dobj`) of the main verb  `<token id="1" lemma="take" pos="VB" surface="take" />`;
	* dependency relations exist only for the English dataset and their tag is consistent with the [Stanford Dependency Tagset](https://nlp.stanford.edu/software/dependencies_manual.pdf).
4. the semantics, based on the Frame Semantics Theory and expressed by Frames (i.e., the `<frames/>` tag) and Frame elements (i.e., the `<frameElements/>` tag):
	* even though a sentence may express an arbitrary number of frames, in the example above only the frame `Bringing` is expressed with two frame elements, i.e., the `Theme` role spanning between the second and the third token (`the mug`) and the `Goal` role, instead spanning between the forth and the seventh token (`next to the keyboard`);
5. the configuration of the environment, in terms of entities populating the Semantic Map (*SM*), along with their semantic attributes (i.e., `semanticMap` tag):
	* each entity is identified by a unique id (`atom`) and characterized by a `type`; in the example above, two objects are in the Semantic Map, such as the object `p1` which is an instance of the class `Cup`;
	* entities are extended through semantic or lexical `<attributes/>`; in the example above an instance of the class `Cup` may contain other entities, so that the `containability` property is `true`; these attributes also encode the multiple lexical references that can be used to refer to the entitie, such as `cup`, `mug` or `bowl`. 
	* entities are localized within the environment through `<coordinate/>` which refer to an ideal gridmap.
6. the gold groundings, providing gold mapping between linguistic symbols (namely, words of the sentence) and entities of the semantic map (i.e., `lexicalGroundings` tag). In the example, the token with id `3` (*mug*) refers to the entity `p1` (`Cup`), while token `7` (*keyboard*) to entity `k1` (`Keyboard`).



## Version

This repository contains the **HuRIC 2.0**. 
The previous version of Huric is available at the following link: [http://sag.art.uniroma2.it/demo-software/huric/](http://sag.art.uniroma2.it/demo-software/huric/)

###Main changelogs with respect to HuRIC 1.0: 
* Added additioanl annotated examples for English.
* Added brand new examples for Italian.
* Each sentence is now paired with a corresponding Semantic Map. 


## Where can I found a processing chain trained over HuRIC?

Together with the corpus, we developed a Spoken Language Understanding system called
LU4R, based on a cascade of sequential labelers, whose models have been trained over HuRIC.
It has been designed also for a context-aware interpretation of spoken commands, consistently with
the corpus. 

More details on LU4R can be found at the following link:: [http://sag.art.uniroma2.it/lu4r.html](http://sag.art.uniroma2.it/lu4r.html)



## How to cite HuRIC

If you use HuRIC for your research, please cite the following paper: 

*Andrea Vanzo, Danilo Croce, Emanuele Bastianelli, Roberto Basili, Daniele Nardi* (2020): **Grounded language interpretation of robotic commands through structured learning**. In: Artificial Intelligence Volume 278, January 2020, 103181, 278, 2020.

```
@article{DBLP:journals/ai/VanzoCBBN20,
  author    = {Andrea Vanzo and
               Danilo Croce and
               Emanuele Bastianelli and
               Roberto Basili and
               Daniele Nardi},
  title     = {Grounded language interpretation of robotic commands through structured
               learning},
  journal   = {Artificial Intelligence},
  volume    = {278},
  year      = {2020},
  url       = {https://doi.org/10.1016/j.artint.2019.103181},
  doi       = {10.1016/j.artint.2019.103181},
  biburl    = {https://dblp.org/rec/bib/journals/ai/VanzoCBBN20},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```


## References

*Andrea Vanzo, Danilo Croce, Emanuele Bastianelli, Roberto Basili, Daniele Nardi* (2020): **Grounded language interpretation of robotic commands through structured learnin**g. In: Artificial Intelligence, Volume 278, January 2020, 103181, 278, 2020.

*Emanuele Bastianelli and Giuseppe Castellucci and Danilo Croce and Roberto Basili and Daniele Nardi* (2017): **Structured learning for spoken language understanding in human-robot interaction.** In: International Journal of Robotics Research, 36 (5-7), pp. 660–683, 2017.

*Emanuele Bastianelli, Danilo Croce, Andrea Vanzo, Roberto Basili, Daniele Nardi* (2016) **A Discriminative Approach to Grounded Spoken Language Understanding in Interactive Robotics.** In Proceedings of the Twenty-Fifth International Joint Conference on Artificial Intelligence, {IJCAI} 2016, New York, NY, USA, 9-15 July


*Emanuele Bastianelli, Giuseppe Castellucci, Danilo Croce, Luca Iocchi, Roberto Basili, Daniele Nardi* (2014): **HuRIC: a Human Robot Interaction Corpus**. In Proceedings of the Ninth International Conference on Language Resources and Evaluation (LREC'14), European Language Resources Association (ELRA), Reykjavik, Iceland, 2014, ISBN: 978-2-9517408-8-4.

*Emanuele Bastianelli, Giuseppe Castellucci, Danilo Croce, Roberto Basili, Daniele Nardi* (2014): **Effective and Robust Natural Language Understanding for Human Robot Interaction**. In: Proceedings of the 21st European Conference on Artificial Intelligence (ECAI 2014), pp. 57 - 62, Prague, Czech Republic, 2014.

