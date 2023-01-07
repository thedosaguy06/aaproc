# aaproc
forenote : ugh i hate this part.

csh 
source cshrc
mkdir 1ga19ec
cd 1ga19ec 

virtuoso &

File -> new-> library -> name it 'ram' -> select attach to an existing tech library (3rd option on rhs));
        OK-> in Technology Library -> select gpdk180 -> OK.


File -> new -> cell View (lib name should be 'ram')-> cell should be 'inv' -> OK.

Schematic window opens .

Create instance(shrtct -> I) -> for Nmos and Pmos ->lib  => gpdk180.
----> NmoS-> total width and finger width => 20ns -> SELECT BODY TYPE .
---->Pmos -> "                          "=> 40ns  -> SELECT BODY TYPE .
---->Create pins vdd a vss etc .SELECT DIRECTION AS INPUT .
---->"               vout    " SELECT DIRECTION AS OUTPUT .




Now -> Create(from taskbar) -> cellView -> FromcellView .( lib name shud be 1ga19 , cell name shud be inv) click OK .

Now pins will appear -> sort where the pins have to go -> left,right,bottom top etc.->OK.

Symbol window will popout. 


Go to virtuoso window -> New -> cellView -> view shud be schematic -> cell name shud be 'inv_tb'. -> OK.


Now, Create -> change library to '1ga19'  and cell to jus 'inv' .-> OK .

Place symbol -> power shud be vdc** and ground shud be gnd . (vpulse??).
-> run ADEL, -> Analyses-> choose -> trans ->  stop time(200n)->CLICK MODERATE->OK.
-> "                             "-> dc    ->  select component-> input .
-> start(0) , stop(1.8)->OK.
-> IN inv_tb schematic window -> trans and dc shud be checked(tick) -> OUtputs-> To be plotted -> select on design-> --
--> sel on iput line and outpt pline .-> play button(netlist and run ) -> Graph will popout -> split the graph .
Calculate dealy and it's done , sheeeeeeeeeeeeesh .



Virtuoso window -> in schematic editor ->  Layout XL.-> create new-> OK.

-> in new file window , OK.
-> Create physical config window will open , press OK .
-> In layout xl window -> Generate ->connectivity-> all from source-> io pins-> darken the label dot , ugh then OK,
-> Layout will come , do that Alli place->pin placement alli click on vdd (top -> hrail) same for vss (bot -> hrail) , OK.
-> Do connections . CREATE VIA MATERIAL NOODKONDU MAADBEKU .
-> go to ASSURA -> TECHNOLOGY -> ...-> .. -> .. -> INSTALL -> FOUNDRY -> ANALOG -> GPDK180 -> RHS ALLI assura Tech.lib -> OK.Apply -> OK .
0->  ASSURA -> TECHNOLOGY -> gpdk180.->OK ,-> OK -> RUN DRC  -> OK .
0-> no error andre close , close .

-> ASSURA -> run LVS-> Technology -> gpdk180 -> OK.
-0> No Problems andre ,OK,

0-> ASSURA -> Run Quantus QRC -> Extraction -> Extraction type(RC) -> Ref Node(0) -> ,OK .

0-> AV_EXTRACTED WINDOW WILL POP OUT -> CLSOE ,
GO TO VIRTUOSO WINDOW , -> change nameof ( Cell -> inv_tb and view to -> av_extracted ,view -> config, Open WITH -> HEIRARCHY EDITOR )., OK.
->USE TEMPLATE -> SPECTRE . change view from (my view to schematic)., OK
-> TREE VIEW -> +(folder hatra)-> sel on folder -> Set Instance View -> av_extracted -> Save . -> click ADE L -> new window pops out .
-> Analyses ->Chose -> trans -> stop time -> 200n ,
-> -> dc -> component parameter -> sel component  from schematic -> sel on vpulse thing -> enabled shud be checked . start(0), stop (1.8),OK. 
******************************???????******************************************


->Tools -> calculator -> clear everything in the big box , sel vt (top left) ,sel i/put pline copy it and paste it in sig 1 similarly for sig 2 and output .
-> append to get ans . 


