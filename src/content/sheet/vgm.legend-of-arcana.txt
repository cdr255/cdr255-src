\version "2.14.2"
\header {
    dedication = \markup { \tiny "Dedicated to Levant and Mahbu." }
    title = \markup \center-column { "Legend of Arcana" }
    subtitle = "From the Playstation Game, Jade Cocoon: The Story of the Tamamayu"
    subsubtitle = \markup { \tiny "Arranged by Christopher Rodriguez" }
    composer = \markup \center-column { "Kimitaka Matsumae" \small "(1998 CE)" }       
    instrument = "For Two Voices and Accompaniment"
    tagline = "This Arrangement Licensed under CC-BY-SA 3.0, for educational purposes only. No Infringement is Intended."
}

 global = {    
       \time 4/4
       \key c \minor
       \tempo 4 = 120
}
     flute = \new Voice  {
       \global
       \set Staff.instrumentName = #"Flute "
       \set Staff.shortInstrumentName = #"F "
       \set Staff.midiInstrument = #"flute"
       g'8 ees''8 |
       c''1~ |
       c''2 s4. g''8 |
       f''1~ |
       f''2. c''8 d''8 |
       ees''1~ |
       ees''2 s4. c''8 |
       g'1~ |
       g'2. g'8 ees''8 |
       c''1~ |
       c''2 s4. g''8 |
       f''1~ |
       f''2. c''8 d''8 |
       ees''4. d''4. c''4~ |
       c''8 aes'4. g'4 ees'4 |
       c'1 |
       s1 |  
     
     }


     ocarina = \new Voice  {
       \global
       \set Staff.instrumentName = #"Ocarina "
       \set Staff.shortInstrumentName = #"O "
       \set Staff.midiInstrument = #"Ocarina"
       s4 |
       s2 c'''16 d'''16 c'''16 bes''16 c'''4~ |
       c'''2 s2 |
       s1 |
       s1 |
       s2 c'''16 d'''16 c'''16 bes''16 c'''4~ |
       c'''2 s2 |
       s1 |
       s1 |
       s2 c'''16 d'''16 c'''16 bes''16 c'''4~ |
       c'''2 s2 |
       s1 |
       s1 |
       s1 |
       s1 |
       s1 |
       }

     harpsichordtreble = \new Voice {
       \global
       \clef "treble"
       \set Staff.midiInstrument = #"orchestral harp"
       \partial 4
       s4 |
       s4. ees'8 g'8 c''8 g'8 ees'8 |
       s4. ees'8 g'8 c''8 g'8 ees'8 |
       s4. d'8 f'8 bes'8 f'8 d'8 |
       s4. d'8 f'8 bes'8 f'8 d'8 |
       s4. c'8 ees'8 aes'8 ees'8 c'8 |
       s4. c'8 ees'8 aes'8 ees'8 c'8 |
       s4. bes8 d'8 g'8 d'8 bes8 |
       s4. bes8 d'8 g'8 d'8 bes8 |
       s4. ees'8 g'8 c''8 g'8 ees'8 |
       s4. ees'8 g'8 c''8 g'8 ees'8 |
       s4. d'8 f'8 bes'8 f'8 d'8 |
       s4. d'8 f'8 bes'8 f'8 d'8 |
       <c' ees' aes'>2. <bes' d' g'>4~ |
       <bes d' g'>2 <g bes ees'>2 |
       s4. ees'8 g'8 c''8 g'8 ees'8 |
       <ees' g' c''>4. <ees' g' c''>4. s4 |
       
       \bar "|."
     }


     harpsichordbass = \new Voice {
       \global
       \clef "bass"
       \set Staff.midiInstrument = #"orchestral harp"
       \partial 4
       s4 |
       c8 g8 c'8 s2 s8 |
       c8 g8 c'8 s2 s8 |
       bes,8 f8 bes8 s2 s8 |
       bes,8 f8 bes8 s2 s8 |
       aes,8 ees8 aes8 s2 s8 |
       aes,8 ees8 aes8 s2 s8 |
       g,8 d8 g8 s2 s8 |
       g,8 d8 g8 s2 s8 |
       c8 g8 c'8 s2 s8 |
       c8 g8 c'8 s2 s8 |
       bes,8 f8 bes8 s2 s8 |
       bes,8 f8 bes8 s2 s8 |
       <aes, ees aes>2. <g, d g>4~ |
       <g, d g>2 <ees, bes ees>2 |
       c8 g8 c'8 s2 s8 |
       <c g c'>4. <c g c'>4. s4 |
       
       \bar "|."
     }

\score {
       \new StaffGroup <<
	 \new Staff << \ocarina >>
         \new Staff <<  \flute >>
	 \new PianoStaff << \harpsichordtreble \harpsichordbass
	 \set PianoStaff.instrumentName = #"Harp "
	 \set PianoStaff.shortInstrumentName = #"H ">>       
>>
       
       \layout { 
       \context { \RemoveEmptyStaffContext }
       }
       \midi { }
}