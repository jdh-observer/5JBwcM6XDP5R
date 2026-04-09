---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.19.1
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

<!-- #region tags=["title"] -->
# Doing Individualism in Post-War Europe. Historicizing Interpersonal Interactions Using Digital Photogrammetry
<!-- #endregion -->

<!-- #region tags=["contributor"] -->
 ### Felix Römer [![orcid](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0009-0001-4974-396X) 
Humboldt-Universität zu Berlin
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["copyright"] -->
[![cc-by](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/) 
© Felix Römer. Funded by Deutsche Forschungsgemeinschaft (DFG Project No. 505139943). Published by De Gruyter in cooperation with the University of Luxembourg Centre for Contemporary and Digital History. This is an Open Access article distributed under the terms of the [Creative Commons Attribution License CC-BY](https://creativecommons.org/licenses/by/4.0/)

<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""} tags=["cover", "figure-GreshamStreet-*"]
from IPython.display import Image 
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "Queue in London, 1984"
            ]
        }
    }
}
display(Image("media/8-Barkshire 1984.png"), metadata=metadata)
```

<!-- #region editable=true slideshow={"slide_type": ""} tags=["disclaimer"] -->
This article benefitted greatly from invaluable advice and technical support I received from the Digital Forensics team at the University of Mittweida, in particular, Sven Becker. Furthermore, I am grateful to Karla Hiltmann for reproducing the Blender model presented in this article. Finally, I thank Jim Lundblad, London, for carrying out field work and physical measurements at 7 Gresham Street.
<!-- #endregion -->

<!-- #region tags=["keywords"] -->
European History, Individualism, Proxemics, Social Theory
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["abstract"] -->
## Abstract

While photogrammetry has been frequently used in the Digital Humanities for three-dimensional reconstructions of material objects from two-dimensional images, this article adapts photogrammetric methods from the applied science of digital forensics to historicize interpersonal interactions between human actors. Applying this methodology, the article investigates changes in personal space preferences during the post-war period by analyzing historical photographs of queues in Western cities. It finds noticeable shifts in spatial behaviour in the second half of the twentieth century. By the early post-war period most people still observed only minimal distances between each other. By the 1970s and 1980s, by contrast, interpersonal distances had markedly increased. The article contends that this development was linked to the rise in popular individualism in Western societies during the same period. The article thus adds a new praxeological perspective to recent research in transnational cultural history on individualization as a fundamental process in contemporary Europe and beyond. In doing so, it strengthens diachronic perspectives in historical praxeology and social theory, and contributes, not least, to interdisciplinary research on interpersonal distance behaviour.
<!-- #endregion -->

## Introduction

<!-- #region citation-manager={"citations": {"6hlai": [{"id": "23314830/MG6B8F75", "source": "zotero"}], "7c377": [{"id": "23314830/ZF97IFLI", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
According to cultural anthropologist Edward T. Hall, personal space is a small invisible ‘protective sphere or bubble’ around our bodies that we maintain in all our social interactions <cite id="7c377"><a href="#zotero%7C23314830%2FZF97IFLI">(Hall, 1990)</a></cite>. Most contemporaries will be familiar with the concept unwittingly or knowingly. In present-day Germany, for example, children are taught in primary schools to respect the imaginary bubbles around their and others’ bodies (http://www.mut-tut-gut-rheinland.de/). In the coronavirus pandemic, state-controlled measures of social distancing heightened awareness of interpersonal distances before personal space practices bounced back to pre-existing preferences once the official restrictions had ended <cite id="6hlai"><a href="#zotero%7C23314830%2FMG6B8F75">(Givon-Benjio <i>et al.</i>, 2024)</a></cite>.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"1txrj": [{"id": "23314830/D3ZL6LXX", "source": "zotero"}]}} -->
Such preferences were also conveyed through popular culture. In a classic episode of Seinfeld from 1994, a celebrated TV programme that became famous for exploring seemingly mundane social practices and norms, Jerry and his friends are startled by a ‘close talker’ who intrudes into the personal space of everybody he talks to (https://www.imdb.com/de/title/tt0697764/). Incidentally, observations of similar situations had sparked Edward T. Hall’s interest in spatial behaviour in the first place: in the 1960s, he worked with American colonial administrators and learned from them that in overseas territories indigenous people frequently ‘stood "too close" during conversations’<cite id="1txrj"><a href="#zotero%7C23314830%2FD3ZL6LXX">(Hall <i>et al.</i>, 1968)</a></cite>, 84.

<!-- #endregion -->

<!-- #region citation-manager={"citations": {"i4ipl": [{"id": "23314830/VBCNRFDN", "source": "zotero"}], "pkcxi": [{"id": "23314830/D84UQWFA", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
While social scientists have explored the variations in spatial behaviour across different cultures, its historical dimension has been largely overlooked. Scholarship in anthropology and other disciplines that followed in Hall’s footsteps has been couched almost exclusively in synchronic framings and has not considered the possibility that patterns of spatial behaviour can change over time <cite id="pkcxi"><a href="#zotero%7C23314830%2FD84UQWFA">(Sorokowska et al., 2017)</a></cite>. More recently, research in literary and cultural studies has brought out historical discourses among philosophers and intellectuals, who developed normative ideas about interpersonal distance (IPD) in response to processes of modernization in Western societies during the twentieth century <cite id="i4ipl"><a href="#zotero%7C23314830%2FVBCNRFDN">(Kolkenbrock, 2023)</a></cite>. While this research has shed much light on the history of IPD on symbolic levels, the historicity of IPD in the material world remains largely unexplored.
<!-- #endregion -->

To explore this gap as a test case for a new method in digital history, this article adapts an established technique from the applied science of digital forensics: it employs methods of photogrammetry and 3D-modelling to produce empirical measurements of IPD from historical photographs depicting social situations. The evidence suggests that during the post-war decades contemporaries in Western societies gravitated towards larger interpersonal distances. The article argues in line with existing social theories that such changes in bodily micro-practices can be regarded both as an indication and as a driving force of wider processes of societal transformation. More concretely, the article posits that the trend of widening IPD can be understood as a form of ‘doing subject’ and can be linked to the rise of popular individualism in Western societies during the 1970s and 1980s.


## Previous interdisciplinary research on IPD and social practices

<!-- #region citation-manager={"citations": {"2j2wr": [{"id": "23314830/GP344UFK", "source": "zotero"}], "6nmkm": [{"id": "23314830/CE4GAGS2", "source": "zotero"}], "jggtl": [{"id": "23314830/C5LH6SJQ", "source": "zotero"}], "k9s8a": [{"id": "23314830/CXANKYF3", "source": "zotero"}], "ndvn8": [{"id": "23314830/FUI6GXK3", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
Edward T. Hall’s pioneering book The Silent Language (1966) provided the first detailed conceptualization of what the author called proxemics, the study of the human use of social space. In his analytical model, Hall distinguished between four concentric zones surrounding the body (intimate, personal, social, public), with personal space delineating the distance maintained in interactions with friends or acquaintances and the larger social space observed in encounters with strangers. Hall’s model has inspired much research in various scholarly disciplines to this day, from anthropology and ethnography to sociology and social psychology, with Hall’s spatial categories often subsumed into the concept of interpersonal distance (IPD) <cite id="jggtl"><a href="#zotero%7C23314830%2FC5LH6SJQ">(Mirlisenna et al., 2024)</a></cite>; <cite id="2j2wr"><a href="#zotero%7C23314830%2FGP344UFK">(McCall, 2015)</a></cite>; <cite id="6nmkm"><a href="#zotero%7C23314830%2FCE4GAGS2">(Hecht et al., 2019)</a></cite>, <cite id="ndvn8"><a href="#zotero%7C23314830%2FFUI6GXK3">(Hayduk, 1983)</a></cite>; <cite id="k9s8a"><a href="#zotero%7C23314830%2FCXANKYF3">(Hayduk, 1978)</a></cite>. 
<!-- #endregion -->

To this day, scholarly interest in the social sciences has concentrated mainly on two related lines of enquiry: firstly, measuring IPD patterns empirically in real-life observations or social experiments, and, secondly, identifying the factors accounting for observable variations in IPD patterns. This research has found that IPD patterns not only depend on the combined individual characteristics of the persons involved in the interactions, including their familiarity with each other, their age, gender, ethnicity, and socioeconomic status, but also on larger social and physical contexts such as the built environments, population densities, climatic and epidemiological conditions, and variations in societal cultures (@sorokowska_preferred_2017; @wohr_mapping_2015).

<!-- #region editable=true slideshow={"slide_type": ""} -->
More concretely, this research has found that two persons who know each other tend to stand closer together during encounters than two persons that have never met before. Importantly, individuals can only choose the distances freely where the physical environment allows this; in crammed physical spaces, for example, on a London Underground train during rush-hour, commuters cannot expect to keep their preferred interpersonal distances. With regards to cultural determinants, societies with high levels of economic prosperity, social inequality, and more individualistic social norms have been associated with preferences for larger IPDs than less affluent and more collectivistic societies. One of the largest recent studies of cross-country IPD patterns has found that the preferred social distance both in Germany and the US stood at more than 90 centimetres in the mid-2010s, while significantly larger distances were recorded, for example, in Saudi-Arabia. By contrast, some of the smallest distances were measured in Argentina (@sorokowska_preferred_2017, table 1).
<!-- #endregion -->

Studies such as these demonstrate the sustained research interest in IPD that has received additional impetus from the experience of the recent coronavirus pandemic. At the same time, the existing body of research reflects the methodological and conceptual limitations of the field. Nearly all previous and ongoing studies have used social experiments, simple questionnaires, or, more recently, computer-based virtual-reality exercises to measure IPD preferences among study participants in artificial settings (@sorokowska_preferred_2017, 9-10). Where researchers have made real-life observations, they have usually resorted to improvised methods such as simple photographs (@ozdemir_shopping_2008). The choice of methodology corresponds to the invariably synchronic framing that has characterized scholarship in proxemics ever since the beginnings in the 1960s. Even though much of this research has been premised on the cultural variability of spatial behaviour, scholars have not drawn the logical conclusion to assume historical variability in IPD patterns and to develop diachronic perspectives on the subject.


Proxemic behavior matters because it can be linked to wider historical processes. The historical significance of seemingly banal social micro-practices – such as personal space preferences – is well established in social theory and recent historical research. In sociological practice theory, it has been argued that social practices represent much more than just individual behavior – they are intricately interwoven with the social world in that they are based on tacit knowledge, cultural codes, norms, and images of society (@reckwitz_kreativitat_2016, 56). As such, they represent elemental building blocks of inextricable formations of practices and discourses; combinations of such formations, in turn, constitute a multiplicity of related clusters, the totality of which form the social world (@reckwitz_kreativitat_2016, 63-4).


In recent years, the practice turn in sociology has also inspired historians to develop historical praxeology as a new methodological approach and field of research. The theoretical advantages of praxeological perspectives are seen in the ability to transgress both structuralist approaches and the methodological individualism inherent in previous social theories: instead, praxeology brings out how the social world is routinely experienced, performed, and transformed through bodily social practices on the micro-level (@freist_historische_2015, 62-3). Methodologically, historical praxeology thus overlaps with recent approaches in the history of the body that are concerned with the relations of human subjects and their bodies with social and material environments (@ruberg_history_2020). The research interest in this field is not only geared towards synchronic analyses of how established practices are performed and understood at particular times, but also towards diachronic perspectives on how practices change over time (@rieske_was_2015).


Nonetheless, it can be argued that synchronic perspectives are still more developed than diachronic perspectives both in historical praxeology and in social theories. Even though leading sociologists have acknowledged the historicity of the social world, societies’ historical dimensions have not occupied a central space in much of the sociological literature (@rieske_was_2015, 205-6; @reckwitz_kreativitat_2016, 65). In particular, few sociologists have offered detailed conceptualizations of the temporalities of social practices and how exactly they undergo transformative processes. According to an existing theory, it is the permanent repetition of routinized social practices in everyday life that opens the door to incremental change: each time a particular bodily routine act is performed in the material world, the physical execution of the movements may deviate more or less slightly from previous rounds (@reckwitz_kreativitat_2016, 61, 100, 123-4, 249-50). As part of larger ‘practice-discourse formations’ (Reckwitz), such changes can not only gradually alter everyday social routines but also form part of and contribute to wider transformative processes in a given society (@reckwitz_spatmoderne_2021, 65, 68, 95-97).


Empirical case studies tracing such incremental changes in past social practices are few and far between, though. In historical praxeology, researchers have been primarily concerned with identifying ‘regularities’, ‘patterns of collective routines’, and ‘formations of social practices’ in particular periods, while there is less research on the precise processes in changes to existing social practices over time (@rieske_historische_2015). This may not least be due to the methodological challenges involved in such an undertaking: it is difficult enough to locate sufficient primary source material to establish regularities in everyday routine acts in a given temporal cross-section (@rieske_was_2015, 212). For example, a recent study on the history of bodily encounters in modern Britain has offered rare insights into the history of personal space by looking, among others, at technical changes to carriage layouts and textual testimonies of passengers on the London Underground, but provides few more direct observations of the practice itself, let alone in quantifiable terms (@koole_how_2016, @koole_intimate_2024). Tracing changes in IPD patterns over time thus offers an opportunity to develop more diachronic perspectives in historical praxeology. 


First inroads into the history of IPD have been made on the analytical level of intellectual ideas. The history of intellectual discourses about ‘the ethics of distance’ has been brought out by recent work in literary and cultural studies (@stan_art_2018; @haustein_alone_2023; @kolkenbrock_ethos_2023). These studies have shown how various influential thinkers of the twentieth century such as Helmuth Plessner, Theodor Adorno, and Roland Barthes engaged in a philosophical quest for the ‘right distance’ in interpersonal interactions. As Katja Haustein has argued, it was primarily in moments of crisis during the twentieth century that intellectuals called for more ‘tact’ in the sense of a mediated way of interpersonal interaction that enables civility and mutual empathy while respecting individual differences and boundaries.


Helmuth Plessner, writing at a time of profound upheaval during the Weimar Republic, advanced the idea of tactful distance as a prerequisite for social and political stability to counter the radical ideologies of community that were pushed both by the far right and the left. For other philosophers and sociologists in later decades, post-war societies were under threat from processes of modernization, consumerism, and new emotional regimes of directness. According to Richard Sennett’s critique (1974), the popularization of psychology and psychotherapy in Anglo-American and European societies engendered hyper-individualist cultures and ‘tyrannies of intimacy’ that undermined the public sphere (@kolkenbrock_ethos_2023, 182). While Sennett bemoaned excessive proximity in social relations in the 1970s, one of his contemporaries, Roland Barthes, instead identified ‘the desire for distance’ in the sense of ‘a desire for personal space’ as a major problem in modern society (@stan_art_2018, 23).


Both a strength and a weakness of this discourse lay in the openness of the underlying definition of distance. This openness was rooted in the historical genealogy of the concept: as a consequence of semantic shifts in English, German, and French discussions during the nineteenth century, the meaning of ‘tact’ was no longer restricted to physical touch or musical rhythm, but was turned metaphorically to describe ‘a particular mode of social interaction’ (@haustein_alone_2023, 16). The breadth of this expanded concept of tact allowed twentieth-century intellectuals to discuss wider trends in social culture, but at the same time it brushed over the differences between various bodily or non-physical forms of social interaction.


The same conceptual openness was reproduced in the recent cultural and literary studies that have explored the intellectual history of tact. Mirroring the original works, this research has referred to the physical, metaphorical, imagined, emotional, and epistemological forms of distance, without making systematic distinctions between these different meanings or operationalizing them analytically (@stan_art_2018, see introduction). Furthermore, with the physical spatiality of social interactions ranging merely as one aspect among others, neither the original works nor the recent analyses have engaged thoroughly with the interdisciplinary literature on IPD, despite the occasional reference to Edward T. Hall.


Lumping together all different forms of distance has logical consequences: it inserts the idea that all forms of social interaction under the umbrella term of tact must follow the same trajectory when it comes to changes over time in social cultures. To use the seemingly paradoxical findings of Sennett and Barthes from the 1970s as an example (#anchor-narrative-para-Helmuth Plessner), it analytically precludes the possibility that the period saw both a trend towards emotional proximity and a trend towards larger interpersonal distances at the same time. As this article will argue, there is much historical evidence to suggest that disentangling the different forms of distance can shed new light on basic trends in sociality and subjectivities in the post-war period.


That distance or nearness was not least a matter of subjectivity has been demonstrated clearly by the recent cultural and literary research on the discourse of tact. Twentieth-century intellectuals of all shades understood distance, although not necessarily in a spatial sense (#anchor-narrative-para-both a strength), as a key variable in the relations of individuals with other persons, groups, or societies at large. Philosophers such as Plessner, Adorno, and Barthes pleaded for distance in defense of individuality, echoing older traditions of bourgeois discourse about the individual vs. the masses (@stan_art_2018, 23; @haustein_alone_2023, 106; @kolkenbrock_ethos_2023, 183).


Respecting the boundaries between the self and the other was regarded as a necessary precondition for recognizing individual differences and individuality more generally. For Helmuth Plessner, in particular, the boundaries of the body were a defining feature of his influential concept of ‘eccentric positionality’: according to this concept, it is the biological boundaries of the body that place the individual human being in a spatial and social environment, and it is the conscious realization of these boundaries that distinguishes humans from other living creatures (@fischer_philosophical_2014). Thus, positioning the individual with their boundary work in his or her environment was a key concern in the intellectual discourse on tact, but this insight has rarely been linked to recent historical research on subjectivities in the twentieth century.


Inspired by the work of Michel Foucault and others, the ways in which subjectivities are made and reshaped in societal processes have not only concerned philosophers and social scientists but also attracted historians (@wiede_subjekt_2020). Moritz Föllmer’s research on twentieth-century Germany has explored the chronology of hegemonic ‘varieties of individuality’ over the course of the century as well as the multiple forms of individuality that existed at any given point; at the same time, the century also saw an overarching trend of individualist expectations extending to all social strata, including the working class (@follmer_individuality_2013, 271-2, 276).


This process accelerated as part of wider processes of modernization in societies during the post-war decades. Based on a complex interplay of socioeconomic, cultural and political developments, it has been argued, the rise of ‘popular individualism’ took off during the 1970s and was reinforced by the neoliberal turn in subsequent decades: as a result, ‘ordinary people’ became ‘increasingly insistent about defining and claiming their individual rights, identities and perspectives’ (@robinson_telling_2017). This process of increasing individualization has been recognized by historians as a fundamental factor in the socioeconomic and political transformation of European societies since the 1970s (@laczo_reconceptualisation_2021).

<!-- #region editable=true slideshow={"slide_type": ""} -->
Importantly, historians have conceptualized this development not as a top-down process but as a more complex interplay involving multiple arenas, levels, and sections of society. On the one hand, ideas about individuality were forged in political, media, and elite discourses (@follmer_individuality_2013, 267, 271-2). The philosophical discourse on the ‘ethics of distance’ can be regarded as part of the latter; during the 1970s, it overlapped with the bourgeoning cultural theories about subjectivity (reckwitz_kreativitat_2016, 69). In the same decade, the concern with questions of subjectivity also met with much popular demand, as became evident in the booming interest in psychology and psychotherapy (@tandler_therapeutische_2016). Ideas about subjectivity and self-hood also inspired social activists and campaign groups who ushered in the era of identity politics in the 1970s – the politics of equality were rooted not only in progressive thought, but also in liberal ideas about individual rights and self-determination (@robinson_telling_2017, 278-9).
<!-- #endregion -->

Not least, individualization was driven ‘from below’ – by ‘ordinary people’, based on vernacular beliefs and performed in everyday life (follmer_individuality_2013, 272). Beginning in the late 1950s, for example, working-class women in Britain pre-empted the feminist movement in developing ideas of their own about selfhood, autonomy, and individuality, a development that was ‘bottom-up as much as it was top-down‘ (@sutcliffe-braithwaite_vernacular_2022, 310). Furthermore, as Florence Sutcliffe-Braithwaite has shown again for post-war Britain, the growing desire for personal autonomy and self-determination went hand in hand with the erosion of social hierarchies and the decline of deference in social culture (@sutcliffe-braithwaite_class_2018). While the rise of individualism did not lead to the collapse of social bonds, it transformed relations between individuals and communities (@lawrence_me_2019). These relations were forged and performed in everyday social interactions of all sorts. Moritz Föllmer has drawn attention to the social and cultural sites in cities where ‘modern individuality was presented, stimulated or indeed created’ (@follmer_sociology_2020, 315). Such insights have recently inspired more historical research into how individualistic ideas were taken up and enacted in sub-cultural activities in daily life during the 1970s and 1980s (@crane_gifted_2022; @steer_emily_2024; whorrall-campbell_emily_2024).


This perspective links back to the social theories discussed above. As Andreas Reckwitz has posited, subjectivities are not only expressed in ideas and narratives, but also produced through bodily practices (@reckwitz_kreativitat_2016, 72-3). Incidentally, empirical evidence in support of this assumption can be found in the psychological literature on IPD that has linked subjectivity to proxemic behaviour (@roeder_selbstkonstruktion_2003). For example, studies have found that more independently-minded persons preferred larger interpersonal distances than people with a less autonomous outlook (@holland_dont_2004). Drawing these theoretical and empirical insights together, I suggest that the intellectual discourse on distance and the material practice of proxemic behaviour can be regarded as interconnected forms of ‘doing subject’.


Operationalizing IPD as a form of ‘doing subject’ enables us to investigate the rise of popular individualism during the post-war period from a new angle. As subjectivity can mean different things in different periods, this approach presumes in line with the aforementioned historical research that subjectivity was widely understood in terms of individuality, especially since the 1960s and 1970s. Thus, I hypothesize that movements in IPD patterns can be interpreted as indicative of shifts in the pervasiveness of popular individualism. Admittedly, there exists no conceivable  possibility of verifying this hypothesis with any certainty, and, theoretically, there may have been other factors at play. After all, the interdisciplinary literature offers a range of different explanations for variations in IPD patterns, as has been noted above. However, there is historical evidence to suggest that, during the period in question, the practice of interpersonal distance was increasingly understood as a matter of self-hood – I will return to this theme below.


## Case study: historical photographs of queues in post-war Europe as a primary source on IPD patterns


As has been suggested in the literature on social theory, source material to study social micro-practices can be obtained from historical photography and film productions (@reckwitz_kreativitat_2016, 57). In order to collect visual evidence of IPD patterns, we narrowed down the search operation to historical photographs depicting queues in twentieth-century European cities. Selecting queues as a case study offers several methodological advantages. As such, lines of multiple queuing people offer the chance to make multiple observations of IPD patterns in the same situation. As a frequently occurring social situation that follows spatial conventions, queues also offer a higher degree of comparability than many other social situations. Furthermore, queues in public urban places are likely to consist of strangers so that the analysis can be limited relatively confidently to the category of ‘social space’.

<!-- #region editable=true slideshow={"slide_type": ""} -->
Finally, it can be argued that queuing resembles the start-stop method that has been widely used in interdisciplinary research on IPD patterns (@wohr_mapping_2015, 298-304). In start-stop experiments, participants are instructed to start walking towards another standing person before stopping at a distance of their own choosing. This setting differs from situations in typical queues only insofar as the persons in start-stop experiments are facing each other, but this difference seems negligible. The IPD literature has conceptualized personal and social space as concentric or elliptical shapes, and frontal distances have been found to be only slightly larger than rear distances – distances kept in queues thus represent minimal interpersonal distances (@hayduk_personal_1983, 297-8; @wohr_mapping_2015, 302). To avoid situations in crammed spaces where people were not free to maintain preferred social distances, I prioritized pictures of relatively small queues with visible tails.
<!-- #endregion -->

The photographic evidence shows unmistakably that IPD patterns changed over the course of the twentieth century. I have found dozens of historical photographs that match my criteria in various digital archives from Germany and Britain. The photographs reveal a clear trend towards larger interpersonal distances. Admittedly, the selection of photographs in my corpus is in no way representative in a statistical sense, but applying statistical representativeness as the sole yardstick would categorically exclude historical photographs as source material for the study of everyday social culture altogether and would not do justice to their analytical potential. Even if the number of eligible photographs is limited, they offer important clues. What seems particularly significant are the striking similarities in the patterns that are visible in the pictures.


To begin with the starkest contrasts, comparing queues from the early twentieth century to queues from a century down the line shows the scale of the changes at a glance. For example, a photograph from 1910 (BPK Kunstbibliothek, Inventory No. WR_00002_18) shows well-dressed people queuing to attend a public trial at a courthouse in Berlin in 1910: people in the queue stand so close to each other that their bodies are almost touching (https://www.bpk-bildagentur.de/shop). By contrast, the Berliners who are lining up for tickets to the Berlinale in a photograph from 2013 stand at arm’s length from each other or even further away (https://www.gettyimages.de/detail/nachrichtenfoto/people-cue-in-front-of-a-ticket-office-for-the-63rd-nachrichtenfoto/160648667?adppopup=true).


The practice of minimal interpersonal distances seemed to have changed very slightly during the first half of the twentieth century. In the early post-war era, the interpersonal distances that Europeans observed in queues appeared to be only gradually larger than before 1945 if at all. A selection of photographs that provide glimpses of this practice over the decades can be accessed here:

```python editable=true slideshow={"slide_type": ""}
!pip install pandas
```

```python editable=true slideshow={"slide_type": ""}
import pandas as pd
```

```python editable=true slideshow={"slide_type": ""} tags=["data-table"]
df = pd.read_csv("media/table1_photographs.CSV",sep=";")
```

```python editable=true slideshow={"slide_type": ""} tags=["data-table", "table-photographs-*"] jdh={"module": "object", "object": {"source": ["LABEL TO ADD"]}}
display(df)
```

```python editable=true slideshow={"slide_type": ""} tags=["figure-Kuenstrasse-*"]
from IPython.display import Image 
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "Queue in Cologne, Kuenstrasse, 1948"
            ]
        }
    }
}
display(Image("media/Kuenstrasse 1948.png"), metadata=metadata)
```

One of the photographs shows women queuing in front of a small local grocery shop at Kuenstraße 7 in the city of Cologne in 1948 (https://www.deutsche-digitale-bibliothek.de/item/P6JO3G3CBVD5E3BTKDSUWNGN4XJ2CXFB). In this case, the fact that the building in the picture still exists enables us to use it as a physical reference point to estimate the interpersonal distances between the women. Judged by the dimensions of various bricks, wall joints and other details it appears that the women observed distances of about 20 centimeters or less between each other. For example, the distance from the corner of the building to the edge of the large window in the centre measures exactly 66,9 centimeters; in the picture, there were two to three women standing in this space.

```python editable=true slideshow={"slide_type": ""} tags=["figure-Kuenstrasse today-*"]
from IPython.display import Image 
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "The still existing building in Cologne, Kuenstrasse"
            ]
        }
    }
}
display(Image("media/Kuenstrasse_Cologne-today.png"), metadata=metadata)
```

<!-- #region editable=true slideshow={"slide_type": ""} -->
More photographic evidence from later years suggests that further and more noticeable increases in interpersonal distances seemed to have occurred in the course of the post-war decades. For example, this evidence includes a picture of a queue of elderly women and men lining up at a pensions office in Kiel in Northern Germany in 1968 (https://fotoarchiv-stadtarchiv.kiel.de/zvimg.FAU?sid=CF7959B2&dm=1&qpos=42876&erg=A&ipos=3&rpos=fotos.jpg&hst=1), or a very orderly queue at a bus stop in Market Street in San Francisco in 1972 (https://www.alamy.com/stock-photo-san-francisco-california-commuters-line-waiting-in-line-for-bus-on-35968950.html?imageid=C48AB9D1-F85C-4B29-B4FB-970B3D9E9D0A&p=105053&pn=1&searchId=086d871b553e2abddfd0f72d7d9fed42&searchtype=0). Another picture shows Londoners queuing in front of a restaurant in the city of London in 1984 (https://historicengland.org.uk/images-books/photos/item/DD002227). Again, it looks as if the people in the queue keep larger distances than people in pictures from the early post-war era or even earlier times, but in order to empirically verify the hypothesis of increasing interpersonal distances during the post-war period, more robust data are required. Therefore, I have used the photograph from London as a pilot study to test the applicability of Photogrammetry for the analysis of social practices in Digital History.
<!-- #endregion -->

## Methodology: a new approach to photogrammetry in digital history

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Photogrammetric techniques have been used since the nineteenth century to extract information from photographs about physical objects such as geographic structures, for example, by means of aerial photography for purposes of topography (@aber_small-format_2010, 23-39). In the digital age, the technique was further developed to enable the creation of digital 3D-models of objects or sites based on two-dimensional pictures. In the Digital Humanities, photogrammetry has been discovered by archeologists, architects, and art historians as a useful tool to produce 3D-models of archeological sites, artworks or museal artefacts (@heijden_replicating_2022; schreibman_textuality_2019). 3D-models have served a range of research and educational purposes, for example, in immersive virtual reality presentations of cultural heritage sites (@rahaman_photogrammetry_2021). To the best of my knowledge, photogrammetry has not been used yet by digital historians to reconstruct social practices depicted in historical photographs.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
In order to explore the possibilities of such an undertaking, we can benefit from existing expertise and experience in Digital Forensics, an applied science that is indeed concerned with locating human actors and their interactions in a given physical space in the context of criminal investigations. In Digital Forensics, photogrammetry has been used for digital reconstructions and 3D-analyses of human bodies and crime scenes (@labudde_computergestutzte_2017). Forensicists employ terrestrial laser scanners to map the geography of crime scenes, before processing the collected geometric data using software applications such as Blender with a view to producing digital 3D-models of the crime scene. These 3D-models can then be exploited to obtain and analyze the measurements of any distances, shapes or other details within the three-dimensional space of the virtual crime scene.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
The method can also be used to analyze two-dimensional video material or stills from CCTV footage, for example, for identifying the exact height of a suspect caught on camera. Finally, photogrammetry can even be used to re-examine photographic evidence from historical criminal cases or so-called cold cases. This scenario comes very close to analytical settings and research questions in Digital History such as ours, but the technical procedure in this scenario is more complicated than in criminological work on contemporary cases.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
What frequently complicates the application of photogrammetry in historical cases, is missing information. Generating a 3D-model requires information about the technical properties of the camera that was used at the time to produce the original historical photograph in question. These parameters include the type of camera sensor, the type of lens, and the degree of lens distortion as well as the position of the camera and its angle in the space where the photograph was taken. This information is indispensable for the production of 3D-models in software applications such as Blender: in a critical work phase called superposition, the two-dimensional picture is linked through a multiplicity of data points to a three-dimensional reference space, a process that requires the configuration of a virtual camera with the same technical properties and spatial position as the original camera.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Both in criminal cold case dossiers and in modern photographic archives, these technical details are often missing. In this scenario, digital forensicists have developed a pragmatic solution to calculate the missing parameters: taking a trial-and-error approach, they feed the software with combinations of parameters in an iterative process until they find a combination where all technical and spatial parameters fit together approximately. This procedure of approximation has been found to be relatively time-consuming but viable. For facilitating the use of photogrammetry for purposes of historical research or cold case investigations in the future, it would certainly be possible to develop a new software tool designed to automating the procedure of approximation, but in the absence of such a tool the procedure has to be carried out manually by trained personnel.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
In any event, building a three-dimensional digital model from a two-dimensional picture requires geometric information. Completing the aforementioned procedure of superposition requires exact measurements of physical reference objects located in the immediate environment of the scene in the picture. These measurements can either be obtained by means of terrestrial laser scanning or manually using a hand-held digital measuring device or even a basic measuring tape. From the combination of measurements at different points in the physical space, Blender can compute a so-called mesh, a three-dimensional network of interconnected data points, which constitutes a 3D-model.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
In a notable exception to the rule, the method of stereophotogrammetry allows spatial analyses of objects in images when more than one picture of the object was taken from different angles: in this scenario, distances or patterns in the image can be computed even without prior scanning or measuring the physical space in the picture. When it comes to historical settings, however, finding more than a single picture of the same scene is a rare occurrence in photographic archives. Thus, applying photogrammetry to single pictures almost always requires information about the physical size of an object or distance in the picture. Obviously, this precondition places limitations on the applicability of this method for purposes of digital history: photogrammetry can only be applied if we know any measurements of material objects in the picture, for example the documented dimensions of a Routemaster double-decker bus in a London street scene or a surviving building that can still be measured.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
In our case study from the city of London, the preconditions for a photogrammetric analysis are all met. The original building in 7 Gresham Street still exists with very little alterations – even the restaurant housed in the building is still in business under the same name. As a requirement for building the digital 3D-model, we defined seven different vertical and horizontal distances at various points of the building’s façade. These distances included, among others, the height of the door frame and the width of the whole front from the left-hand edge of the large windows all the way to the edge of the window on the right-hand side. The measurements of these distances were taken by a London-based IT-specialist with experience in 3D-modelling, using a hand-held digital measuring device (Bosch PLR 40 C).
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""} tags=["figure-Gresham Street today-*"]
from IPython.display import Image 
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "The still existing building in London, Gresham Street"
            ]
        }
    }
}
display(Image("media/photo_piccolo bar-2020.png"), metadata=metadata)
```

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
The original photograph was the work of a London-based photographer, Paul D. Barkshire (@barkshire_paul_paul_nodate), and is located in the digital collections of the Historic England Archive (https://historicengland.org.uk/images-books/photos/item/DD002227. For the specifications of the camera that was used to take this picture, I was able to obtain the necessary details such as the make of the camera, the lens, and the film, directly from Paul D. Barkshire who kindly responded to an email enquiry (camera: Eastman View No. 2 (c.1920), lens: 300 mm Nikon 1:9, film: Kodak Tri-X E.I.125 (8x10), exposure: 1/8 sec, f/16).
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
In order to link the original photograph to a digital three-dimensional reference space we uploaded the picture and fed the collected data into the software application Blender. Some essential parameters remained unknown. As the original position and rotation of the camera was impossible to determine with any precision, the work phase of superposition required manual approximation using an iterative trial-and-error procedure as described above. This work phase took an experienced digital forensicist about two working days to complete. As a result, a coherent 3D-model of the scene in the picture was produced in which all parameters were balanced out approximately. The details of the 3D-model with all specifications can be accessed here:
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
[Download: 3D model of London street scene, 1984 (Blender)](https://github.com/jdh-observer/5JBwcM6XDP5R/blob/main/media/Barkshire1984_Modell.blend)
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
The resulting 3D-model from our pilot study can now be used to determine any physical distances that occurred in the original situation at 7 Gresham Street on 17 July 1984, including the interpersonal distances between the people in the queue. Interpersonal distances were read from the 3D-model in Blender using visible parts of faces and shoes as anchor points between various pairs of persons in the queue. The analysis shows that one of the men in the queue kept a distance of 40 centimeters from the man in front of him. The only woman in the queue even maintained a distance of 76 centimetres from the man in front of her. Compared to the patterns found in pictures from the 1940s and 1950s, the interpersonal distances in this case appear to be significantly larger and thus seem to corroborate our hypothesis.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""} tags=["hermeneutics", "figure-blender-*"]
from IPython.display import Image 
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "Screenshot form the 3D model in Blender with measurements"
            ]
        }
    }
}
display(Image("media/screenshot2.png"), metadata=metadata)
```

<!-- #region editable=true slideshow={"slide_type": ""} -->
## Historical praxeology of personal space preferences since the post-war era
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
As our photogrammetric analysis suggests, there is evidence of a trend towards larger interpersonal distances in European and Western societies during the post-war era. Theoretically, it would be possible to narrow down the chronology of this trend more precisely by undertaking more photogrammetric analyses, time and resources permitting. For the time being, the hypothesis seems plausible, in light of the available photographic source material discussed above, that this trend can be placed preliminarily in the temporal context of the 1960s and 1970s. As this article argues, the trend towards larger personal space was rooted in the secular process of individualization and linked to the rise of social activism and body politics in this period.
<!-- #endregion -->

The process of individualization in the 'Western' world is all but impossible to disentangle from economic and material developments in the post-war period. As Frank Trentmann has argued, one of the key words of the 1960s and 1970s was the ‘self’, and this new orientation towards self-determination was based on a pervasive material transformation of everyday lives. Economic growth during the post-war boom brought about affluence, consumerism, and a ‘simultaneous expansion of leisure time, education, flexible jobs, media, and mobility’ (@trentmann_out_2024, 251-2).


Affluent citizen-consumers got used to more generous housing standards and living arrangements with increasing amounts of square meters and rooms per person – a development that went hand in hand with new norms and expectations of individual privacy (@trentmann_empire_2016, 236-51; @trentmann_evolution_2018, 837). Furthermore, the complex mixture of factors that reflected and contributed to the rise of popular individualism also included secularization, changing and more permissive social norms and family values, the erosion of traditional collectivistic class identities, and, not least, the explosion of ‘identity politics’ and new social movements (@robinson_telling_2017, 272-5).


The latter requires more elaboration. Importantly, this is not to make any monocausal arguments about the rise of popular individualism and concomitant personal space preferences but to explore the ways in which both phenomena were linked through contemporary discourses and social practices. As this article contends, an important connection was made by feminist body politics in the 1970s.


The rise of body politics in connection with second wave feminism has been a major theme in recent research at the intersection of gender history and the history of the body. This research has demonstrated that it were burning questions surrounding the female body that inspired the second wave of feminism in the last third of the twentieth century in the first place (@schmincke_korpersoziologie_2021, 120-1). Feminists recognized the female body as a central site where unequal gender regimes were forged and enforced through dominant patriarchal practices depriving women of their rights to bodily autonomy, reproductive and sexual self-determination. Ultimately, women’s entitlement to individuality and participation in society was regarded as resting on full authority over their own bodies. Consequently, feminists politicized what was previously regarded as private: domestic abuse, sexual violence and, above, all, abortion rights became key issues in the transnational feminist movement in the late 1960s and 1970s (@lenz_neue_2008). Accordingly, feminist campaigns for these rights have also occupied a central space in modern historiography.


A lesser-known contribution by feminists to contemporary understandings of the body and the self lay in their re-conceptualization of proxemic behaviour as a gendered form of social interaction. As feminist scholars and activists set out to de-essentialize the allegedly natural differences between male and female bodies, they explored a broad range of bodily perceptions and micro-practices. Even the smallest and seemingly unpolitical physical movements such as throwing a ball, feminists argued, were not determined biologically but ultimately shaped by patriarchy. In this context, feminists also took inspiration from Edward T. Halls theory of proxemics.


An early example of the feminist version of proxemics was offered by the American activist and writer Rita Mae Brown. In 1974, she used a journal article to elaborate on gender inequalities in spatial behaviour and called on the feminist movement to take the matter up (@brown_good_1974). Referencing Edward T. Hall’s classic book The Silent Language, she observed that in the presence of men, women moved differently and took up smaller proportions of physical space than men. These differences in behaviour, Brown explained, were instilled in girls and women through education and thus represented a manifestation of unequal power relations in society. For Brown, studying and overturning this practice was thus a deeply political matter: ‘Women and men are taught to use space quite differently, and we need an in-depth study of this by feminists. […] As the feminist demands more physical space and reclaims her strength, so too, she seeks increased political space.’


On the back of the increasing scientization of the feminist movement, gendered spatial behaviour became a recurring theme in scholarship and activism on women’s issues. The subject was taken further in an influential article by American political scientist Iris Marion Young in 1980. In line with previous thought, she argued that girls and women were conditioned from early childhood to more limited uses and movements of the body than boys and men, for example, in physical education (@young_throwing_1980). These limitations also extended to everyday social interactions. As Young observed, women tended not to fully take up the available physical space; instead they often withdrew to a smaller space behind an invisible barrier as if to create a buffer zone for protection against male intrusions into their personal space. Such intrusions, Young claimed, were something that women had to suffer on a daily basis: ‘The most extreme form of such spatial and bodily invasion is the threat of rape. But we are daily subject to the possibility of bodily invasion in many far more subtle ways as well.’


The feminist discourse on gendered proxemics contributed to a new awareness of personal space. While sexual violence and other forms of harassment such as groping that involved physical touch certainly absorbed more attention in public discourse than non-tactile intrusions of personal space, the latter was widely understood as a variation of the former. After women in the US broke silence over sexual harassment in the workplace in the mid-1970s, the issue was also investigated by feminists in other countries such as West Germany. A major report published in 1984 demonstrated the sheer scale and the many forms of sexual harassment. It focused primarily on physical and verbal abuses but also included testimonies of women complaining about men ‘getting too close’ (@plogstedt_ubergriffe_nodate).


Perhaps the most striking visualization of gender inequalities in proxemic behaviour was delivered by West German artist Marianne Wex. In the mid-1970s, she embarked on a photographic and media study of body languages that resulted in a large collection with thousands of pictures juxtaposing male and female postures in everyday situations. In her commentary, Wex drew particular attention to differences in spatial patterns: men were frequently seen spreading out over larger spaces than women who usually kept their arms, legs, and shoulders closer together. Wex interpreted this posturing as ‘the physical expression of men’s psychological and economic occupation’ of society (@wex_sprache_1977). With her artistic activism, Wex contributed to transnational feminist discourse in West Germany and beyond. Her pictures went on display in contemporary art exhibitions and have been shown again in international venues since the 2000s and 2010s (https://www.moma.org/collection/works/284789). An English-language edition was published in 1979 and included a call for action under the fitting title ‘Let’s Take Back Our Space!’


In other words, feminists around the world called on women to defend or even expand their personal space, a suggested behaviour that can be described in analytical terms as a form of ‘doing gender’. At the same time, it can also be interpreted as a form of ‘doing individualism’. After all, feminists understood personal space as a matter of individuality and individual rights. Furthermore, as has been noted above, the politicization of personal space since the 1970s coincided with philosophical discussions about the ‘right distance’ in interpersonal interactions and other scholarly and public discourses that were concerned with subjectivity and self-determination. It may not have been a coincidence that the 1970s also saw a boom in research on proxemics (hayduk_personal_1983, 293).


On the material level of everyday social practice, people in Western societies during the same period developed preferences for larger interpersonal distances, as our photogrammetric analysis suggests. Incidentally, research in the social sciences also detected effects of the feminist movement on non-verbal body languages, including spatial behaviour (@mayo_gender_1981, 256-8; @horgan_nonverbal_2024). It is noteworthy that the impact of feminist demands to take back social space could have the paradoxical effect of actually reducing interpersonal distances – in that women emboldened by feminist thought began to break through invisible barriers and used space more confidently up to the point of violating men’s personal spaces (@tipton_invasion_1975). In the end, both in practice and in discourse, the message was clearly that personal boundaries ought to be respected.


Admittedly, there is no way of verifying any links between social practices and intellectual discourses with any certainty, but, according to existing social theories, this lies in the nature of things. If we accept that social practices are based on tacit knowledge, it follows that these implications cannot be accessed by historians directly; conversely, we cannot observe empirically if discursive norms ever inspired actions. Theoretically, we can only make more or less plausible assumptions about such linkages based on indirect evidence, presuming that practices and discourses do not represent separate entities but different symbolic and material manifestations of the same cultural knowledge orders (@reckwitz_kreativitat_2016, 61-2).

<!-- #region editable=true slideshow={"slide_type": ""} -->
## Conclusion
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
While photogrammetry has been frequently used in the digital humanities for three-dimensional reconstructions of material objects, this article has adapted photogrammetric methods from the applied science of digital forensics to historicize interpersonal interactions between human actors. Applying this methodology, the article has investigated changes in personal space preferences during the post-war period by analyzing historical photographs of queues in West European cities. It has found noticeable shifts in spatial behaviour in the second half of the twentieth century. In the early post-war period most people observed only minimal distances between each other. By the 1970s and 1980s, by contrast, interpersonal distances had markedly increased. The article contends that this development was linked to the rise in popular individualism in Western societies during the same period. The article thus adds a new praxeological perspective to recent research in transnational cultural history on individualization as a fundamental process in contemporary Europe and beyond.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
Historicizing social micro-practices contributes to diachronic perspectives in historical praxeology and social theory. By introducing a historical perspective on personal space, the article also expands existing interdisciplinary research on proxemic behaviour. Methodologically, it could transform research on interpersonal distance behaviour in the social sciences that has previously relied almost exclusively on artificial social experiments. In contrast to questionnaires, laboratories, or virtual reality environments, photogrammetry offers a way of obtaining new data on interpersonal distance patterns in real-life situations.
<!-- #endregion -->


