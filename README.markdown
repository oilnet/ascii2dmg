Synopsis and Usage
==================

ascii2dmg takes a text file such as a [Markdown](http://daringfireball.net/projects/markdown/) file and replaces everything inside twin brackets "[[...]]" following a specific ASCII-only format of typing the DMG transliteration of Arabic with the actual Unicode characters that would have had to be used. The DMG transliteration standard is described in [DIN 31635](http://en.wikipedia.org/wiki/DIN_31635). ascii2dmg was born out of my habit of typing lecture notes on my mobile phone, where there is no chance of efficiently using the Unicode characters. If you use any of the more popular light markup formats you can first pipe your text through ascii2dmg and then [Pandoc](http://johnmacfarlane.net/pandoc/) to get an ODT, LaTeX, HTML or whatever you fancy.

The DMG ASCII-only representation works as follows:

~~~~~~~~~~~~~~~~~~~~~~~
Arabic  DMG   ASCII-DMG
ء/ا     ʾ/ā     )/a-
ب       b       b
ت       t       t
ث       ṯ       t_
ج       ǧ       g^
ح       ḥ       h.
خ       ḫ       h_
د       d       d
ذ       ḏ       d_
ر       r       r
ز       z       z
س       s       s
ش       š       s^
ص       ṣ       s.
ض       ḍ       d.
ط       ṭ       t.
ظ       ẓ       z.
ع       ʿ       (
غ       ġ       g.
ف       f       f
ق       q       q
ك       k       k
ل       l       l
م       m       m
ن       n       n
ه       h       h
و       w/ū     w/u-
ي/ى     y/ī     y/i-
~~~~~~~~~~~~~~~~~~~~~~

For an actual hiven ("-"), a slash ("/") should be used. Uppercase letters are supported as well but left out of the above table for brevity. To give an example: بسم الله الرحمن الرحيم is transliterated into DMG as bismi-llāhi r-raḥmāni r-raḥīm and would be written [[bismi/lla-hi r-rah.ma-ni r-rah.i-m]].
