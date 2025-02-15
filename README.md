# Text-Metaphone-Amharic
The Metaphone Algorithm for Amharic.

## Overview
This is reimplementation of the Amharic Metaphone algorithm
of the `Text::TransMetaphone package`.  This implementation uses
an object oriented interface and will generate keys in
Ethiopic script by default.  IPA keys remain available and
may be set at instantiation time or after wards.  See the POD
for details.

The script `examples/matchtest.pl` will perform matching on
a group of 116 correctly spelled words compared against 166
misspelled words in 9 misspelling categories.  In a few cases
the misspelled words go outside the scope of what the Metaphone
algorithm is intended for.

The `Text::Metaphone::Amharic` algorithm does produce better
results than the alternatives.  What alternatives? :-)  The
only somewhat sensible comparison would be to transliterate
Amharic into an ASCII system and apply the DoubleMetaphone
to the converted words.  Results for 4 transliteration systems
are as follows ("low" granularity setting):


Text::Metaphone::Amharic (Ethiopic)
	- 116 canonical words matched 160 of 166 error words.

Text::DoubleMetaphone (SERA)
	- 116 canonical words matched 105 of 166 error words.

Text::DoubleMetaphone (Ethiop)
	- 116 canonical words matched  99 of 166 error words.

Text::DoubleMetaphone (ISO)
	- 116 canonical words matched  97 of 166 error words.

Text::DoubleMetaphone (Mainz)
	- 116 canonical words matched  89 of 166 error words.
