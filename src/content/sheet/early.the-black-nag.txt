\version "2.7.40"
\header {
	tagline = "Arranged by Christopher Rodriguez"
	subtitle = "An English Country Dance by John Playford"
	subsubtitle = "(1651 CE)"
	title = "The Black Nag"
}
voiceB =  {
\set Score.defaultBarType = "empty"

% %MIDI program 0

\time 6/8 
\partial 8
\repeat volta 3 {   

e'8 \bar "|"
a'4 a'8 b'8 a'8 b'8 \bar "|"
c''8 b'8 c''8 d''8 c''8 d''8 \bar "|" 
e''8 d''8 c''8 b'8 c''8 b'8 \bar "|" 
a'4 ~ a'16.  s32 a'4 e'8 \bar "|"
 
a'4 a'8 b'8 a'8 b'8 \bar "|" 
c''8 b'8 c''8 d''8 c''8 d''8 \bar "|" 
e''8 d''8 c''8 b'8 c''8 b'8 \bar "|" 
a'4 ~ a'16.  s32 a'4 a'8 \bar "|" 

b'8 g'8 e'8 b'8 g'8 e'8 \bar "|" 
b'8 g'8 e'8 b'8 c''8 d''8 \bar "|" 
e''8 c''8 a'8 e''8 c''8 a'8 \bar "|" 
e''8 c''8 a'8 e''8 d''8 c''8 \bar "|" 

b'8 g'8 e'8 b'8 g'8 e'8 \bar "|" 
b'8 g'8 e'8 b'8 c''8 d''8 \bar "|" 
e''8 d''8 c''8 b'8 c''8 b'8 \bar "|"
a'4 ~ a'16.  s32 a'4 a'8 \bar "|" 

b'8 g'8 e'8 b'8 g'8 e'8 \bar "|" 
b'8 g'8 e'8 b'8 c''8 d''8 \bar "|"
e''8 c''8 a'8 e''8 c''8 a'8 \bar "|"
e''8 c''8 a'8 e''8 d''8 c''8 \bar "|" 

b'8 g'8 e'8 b'8 g'8 e'8 \bar "|"
b'8 g'8 e'8 b'8 c''8 d''8 \bar "|" 
e''8 d''8 c''8 b'8 c''8 b'8 \bar "|"
}
\alternative {
{  a'4 ~ a'16.  s32 a'4 \bar "|"}
{  a'4 ~ a'16.  s32 a'4. \bar "||"}
} 

} 
voicedefault = { \set
		 Score.defaultBarType = "empty"
		 
		 \time 6/8 \tempo  4=180
		 \key a \minor 
	       }

\score{
  <<
    
    \context Staff="1"
    {   
      \voicedefault
      \voiceB 
    }
    
  >>
  \layout {
    \context {
    \Score
    \override SpacingSpanner #'base-shortest-duration = #(ly:make-moment 1 32)
  }
  }
  \midi {}
}
