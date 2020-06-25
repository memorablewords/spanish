<br /><br />

<p align="center"><code>corrector caballo pila grapa tiempo cielo</code></p>

<br />

<h1 align='center'>Spanish Wordlist(s) for Random Passphrases</h1>

<p align="center">Wordlists in Spanish suitable to generate memorable passphrases.</p>

<br /><br />

> **Work in progress**: the list isn't quite ready for publication yet, but you can read about the work in progress below!

<br /><br />

1. [Motivation](#motivation)
2. [Methodology](#methodology)
   1. [Existing wordlists](#existing-wordlists)
   2. [Design goals](#design-goals)
   3. [Source of words](#source-of-words)
   4. [Process](#process)
3. [References](#references)

Motivation
----------

Using words from a language that you don't understand defeats some of the strategies you could employ to remember a passphrase. Ideally, everyone would have access to wordlists in languages of their choice.

Methodology
-----------

This project methodology is based on the observations published by the Electronic Frontier Foundation (EFF) in [Deep Dive: EFF's New Wordlists for Random Passphrases][jbonneau2016].

These observations improve on the wordlists originally published with the [Diceware][diceware] method for creating passphrases by Arnold G. Reinhold.

  [jbonneau2016]: https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases
  [diceware]: https://www.eff.org/dice


### Existing wordlists

The Diceware website provides lists in multiple languages, including [two wordlists in Spanish][mp2003], the design of which was documented by their author (see [References](#references)).

####  DW-Español-1.txt

The first wordlist was designed with a focus on brevity and portability:

- 3.3 characters per word on average
- only uses characters which ASCII values are < 127

#### DW-Español-2.txt

The second wordlist was designed with a focus on brevity and memorability, and introduces more words that would be familiar to a Spanish speaker (and includes characters with [diacritical marks][diacritic]):

- 4.4 characters per word on average
- larger proportion of meaningful Spanish words

**Note**: In line with the main goal of brevity, both lists contain case variations of short words as well as variations that only differ by their diacritical marks. Both lists also contain words composed only of punctuation and symbols.

  [diacritic]: https://en.wikipedia.org/wiki/Diacritic

### Design goals

#### User research

It is generally difficult to memorize words in any language without being to some extent familiar with that language.

The population of Spanish speakers (and writers) is both large and diverse. People use overlapping vocabularies in different parts of the world.

The overwhelming majority of people I know who type in Spanish do not change the layout of keyboards they use only occasionally. They give up writing diacritics instead (sometimes at the cost of clarity or additional typing).

Spelling in Spanish is a challenge for many people. Diacritics can be difficulties, as well as the spelling of homophonic characters (e.g. _casa_: house and _caza_: hunt are homophones in Latin America).

#### Design goals

1. **Usability**: I want the experience of inputting my passphrase to be as familiar as possible, no matter the situation.
2. **Memorability**: As much as possible, I want to avoid situations of doubt when recalling my passphrase.
3. **Inclusiveness**: Everybody should have access to passphrases they can feel are theirs to use when they need them.
4. **Brevity**: I want to do as little as necessary to input my passphrase.

#### Design guidelines

1. Only words that don't contain any letter with diacritical marks: **á é í ó ú ü ñ**.
   - **usability goal**: reduce the impact of different keyboard layouts on the experience of typing my passphrase
   - **brevity goal**: diacritics often require additional keystrokes

2. Only lowercase, meaningful words—no symbols, no digits.
   - **usability goal**: lowercase letter keys are usually among the easier to access
   - **memorability goal**: meaning and connotation make words easier to distinguish than numbers or series of symbols
   - **brevity goal**: mixed-case letters usually require additional keystrokes

3. As much as possible, no profane, insulting, sensitive, or emotionally-charged words.
   - **inclusiveness goal**: not including words with meanings, common uses, or connotations that no one would miss in their passphrases makes for a tool that more people could feel happy to use.

4. As much as possible, words recognized by many people—at the very least words that can be found in an average dictionary
   - **memorability goal** _I attempted to select words that would be more commonly recognized by different groups of people (whether they use them or not) while embracing the fact that Spanish is a diverse language used by a diverse group of people._
   - **inclusiveness goal**: _I attempted to take into account that we all have biases and that the_ CORPES XXI _data set does indeed reflect some of the most common._ (See [Source of words](#source-of-words).)

5. As much as possible words with concrete meanings.
   - **memorability goal**: I assume this is why Joseph Bonneau ranked the wordlist candidates by "concreteness". I used this criteria mostly when removing words that would have been more easily understood as adjectives than nouns. (See [Process](#process).)

6. Words as short as reasonable.
   - **brevity goal**: the length of the words won't affect the strength of the passphrase


### Source of words

The [Royal Spanish Academy][rae] makes publicly available statistics about a reference corpus of contemporary texts (CORPES XXI), including the list and frequencies of [lemmas][lemma] found in the corpus.

The [proposed word list][long] is based off the most frequently used words in that corpus.

> _ISSN 2340-941X Corpus del Español del Siglo XXI (CORPES)_, version 0.92, published in May 2020. ([main page][corpes], [statistics][stats], [data source][data])
>
> _For what is worth, at the time of sourcing the SHA-1 hash of `corpes_lemas.zip` was `4520a17688edfb52c008e1bb87135f5ee5727f46`._

  [rae]: https://en.wikipedia.org/wiki/Royal_Spanish_Academy
  [lemma]: https://en.wikipedia.org/wiki/Lemma_(morphology)
  [corpes]: https://www.rae.es/recursos/banco-de-datos/corpes-xxi
  [stats]: http://web.frl.es/CORPES/org/publico/pages/estad/estad.view
  [data]: http://web.frl.es/CORPES/estad/corpes_lemas.zip

### Process

I took the 9000 most frequently used 3 to 9-letter-long **verbs** and **nouns** without diacritics, from CORPES XXI then manually checked and attempted to remove as many profane, insulting, sensitive, or emotionally-charged words as possible.

I also selectively removed alternative forms when they wouldn't have a distinct meaning (e.g. plurals or diminutive nouns unless they would evoke a distinct meaning from the meaning evoked by their singular or regular form).

No word in the list is an exact prefix of any other. That sometimes meant prioritizing two or three slightly longer words over a single short one.

The boundary between adjectives and nouns is sometimes blurry in Spanish when there is no context, and I attempted to remove forms less likely to be recognized as nouns, thus prioritizing standalone concrete words.

I also removed homophones when I found them, and I avoided doubling gendered forms, while at the same time attempting to balance the roles represented by gendered words.

Finally, I completed the list with a subset of the 1500 most frequently used 10-letter words without diacritics, and followed the same guidelines described above.

_Note: those final adjustments are still in progress, so I'll update the process description when they're done._

References
----------

- Electronic Frontier Foundation (EFF), Joseph Bonneau: [Deep Dive: EFF's New Wordlists for Random Passphrases][jbonneau2016]
- Miguel Palao: [Listas Diceware en Español][mp2003]—[DW-Español-1.txt][mp2003-1] and [DW-Español-2.txt][mp2003-2]. [Design document][mp2003-design] (in Spanish) [2003]
- REAL ACADEMIA ESPAÑOLA: Banco de datos (CORPES XXI) [en línea]. _Corpus del Español del Siglo XXI (CORPES)._ http://www.rae.es [2020-06-14]

  [mp2003]: http://world.std.com/~reinhold/diceware_espanol/listas_diceware_en_espanol.htm
  [mp2003-1]: http://world.std.com/~reinhold/diceware_espanol/DW-Espanol-1.txt
  [mp2003-2]: http://world.std.com/~reinhold/diceware_espanol/DW-Espanol-2.txt
  [mp2003-design]: http://world.std.com/~reinhold/diceware_espanol/GeneracionDW-Espanol.pdf
