# Week Three

In this weeks activity I had the task of understanding basic encoding standards for musical data. In this activity I focused on generated both MusicXML and MEI files and experimenting with rending and modifying these MEI files.

You can access my MUSIC.XML file [here](MUSIC.XMLFILE)

You can access my MEI file [here](https://mei-friend.mdw.ac.at/)

In terms of the differences within the elements between XML and MEI, the first noticeable one is the different structures both types of files individually follow. The types of files both inscribe note values in sheet music differently for example XML is like:

  [<chord/>
        <pitch>
          <step>A</step>
          <octave>4</octave>
          </pitch>
        <duration>4</duration>
        <voice>1</voice>
        <type>half</type>
        <stem>up</stem>
        <staff>1</staff>
        </note>]


    Whereas MEI is like so:

    <layer xml:id="l1swo76w" n="1">
                           <chord xml:id="cmtolve" dur.ppq="4" dur="2" stem.dir="up">
                              <note xml:id="n1m6pgd6" oct="4" pname="e" />
                              <note xml:id="nffhasm" oct="4" pname="a" />
                              <note xml:id="n1xa7jda" oct="5" pname="c" accid.ges="s" />
                           </chord>
                           <note xml:id="n1g8c607" dur.ppq="4" dur="2" oct="5" pname="d" stem.dir="down" />
                        </layer>
                     </staff>

                    
