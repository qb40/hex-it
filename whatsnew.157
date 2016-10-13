
HexIt v1.57 (C) 1995-2001 Mikael Klasson
fluff@geocities.com
http://mklasson.cjb.net

Dates are YYMMDD, times are 24h GMT+1, just like they _should_ be! ;)

If you really want to know what's going on inside HexIt, then please
read this file! It's pretty thorough at times...

Some entries are prefixed with 2 letters and a colon. These letters tell
you what mode the entry applies to.
	TM = TextMode
	HM = HexMode
	DM = DumpMode
	CM = CodeMode


                         ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
                         ³v1.57 - 10 Sep 2001³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[010910] Win32: Setup->[Define Keys] didn't work.
[ 00.40]

[010910] Win32: hexitw.exe didn't accept filenames with spaces in them 
[ 00.00] (i.e. quoted filenames).

[010607] HM: "Fill selection" in InsertValue didn't work properly; it 
[ 06.00] started filling from the current position instead of the selected 
         blocks beginning. Thanks to Sune Marcher!


                         ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
                         ³v1.56 - 28 May 2001³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[010528] Aaah... loading more than two files under win32 didn't work very
[ 20.30] well. A little pointer got mixed up and before you knew it all 
         hell broke loose. This problem also cropped up when having two 
         files loaded and cutting bytes from the first one, and probably in
         a number of other situations as well. A nasty bug, I tell you.

[010528] Fixed some bug that reared its ugly head when aborting a LoadFile
[ 17.00] and not having any other files loaded.

[010527] The percentage indicator was wrong in HM, DM, and CM at offsets
[ 21.10] larger than 42949673. It seems I ignored the high 32 bits of the 
         calculations.

[010527] HM: CursLeft in the text field was sensitive to the NibbleMove
[ 20.00] setting due to a nasty little register typo.

[991206] Navigating after the 1280000:th line in TextMode was very
[ 06.00] sluggish. I keep a buffer of limited length where I store the
         offsets for each 256:th line. I've doubled that buffer now, so
         things will still be sluggish eventually - though this time
         after 2.5 million lines. Not the best solution, I know, but a
         simple one. Yes, I've recently started looking at 150 meg
         files. :-)


                         ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
                         ³v1.55 - 03 Dec 1999³
                         ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[990710] HM: Oh my. I was browsing through some old mails today and came
[ 09.10] across a 7 months old bug report by a Good HexIt User (GHU
         (tm)). In it he tells me of a problem related to PutSelection
         (<Ctrl>+<F2>), namely that it seems to write one byte too many
         when selecting past the last byte. This happens if you just
         press <Shift>+<End> for example. I've managed to get my act
         together for a few minutes and fix that particular problem now.
         Let's just hope he forgives me. :)

[990722] Oops. HexIt would probably have come crashing down if you tried
[ 16.30] starting it without any hi memory available. I'm not saying it
         won't now, I'm merely saying the risk is smaller. ;)

[990726] HM: Hrrm. If you tried inserting more bytes with InsertValue
[ 17.50] than you had available memory, HexIt merrily continued into
         non-existent memory. Guess I was tired when I wrote it, eh?
         Suuure...

[990726] HM: When comparing files, HexIt never found a match on the last
[ 18.00] byte.

[990726] HM: Using InsertValue at the end of a file produced some
[ 19.20] strange behaviour.

[990727] Previous versions didn't set the archive flag when creating
[ 16.00] files. Not that big of a deal perhaps, but since everyone seem
         to do it, I figure I may as well do it as well as well [sic].

[990727] CM: HexIt didn't recognize the two bytes long "pop reg"
[ 16.40] instructions at 08fh,0c0h. Quite useless ones, but they're in
	 for the sake of completeness now.

[990730] CM: Fixed a bunch of problems with word sized immediate
[ 14.50] operands in 32-bit mode.

[990730] CM: Instructions with 32 bits offset only weren't assembled
[ 15.40] correctly in 32-bit mode.

[990807] CM: "cmp" is now included in the set of instructions that get
[ 20.30] comments with "Some comments".

[990809] CM: "prefetch" and "prefetchw" are now recognized as separate
[ 17.40] instructions. ("prefetch" was always used earlier)

[990811] HM: Pasted bytes weren't selected when destination file
[ 22.40] differed from source file.

[ 23.00] HM: GetBlock didn't set the FileChanged flag when overwriting
	 previous data.

[990812] HM: Every 1024th occurrence was ignored when replacing shorter
[ 03.50] strings with longer ones. As if that wasn't enough, you also
	 had to press a key to wake up hexit again after every skip. I
         took the time to speed up the replace routine a bit - sometimes
         by as much as a factor of 3 - at the expense of less frequent
         <Escape> polling.

[ 04.00] HM: Cutting or copying a block when a marker was set after the
	 last byte copied one too many bytes.
	 
[991203] Wee! I've finally gotten around to releasing a win32 version of 
[ 05.40] HexIt. It's been in this state for the last several months, so 
	 it's really quite a pity I haven't released it until now. I'm 
	 just hoping it'll work fine now, otherwise my previous sentence 
	 will look rather foolish. ;) Anyway, I'm expecting a few bugs 
	 and stuff like that. Consider this initial version a beta.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.54 - 21 May 1999³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[990310] It seems I've just had my annual really-long-break-from-hexit.
[ 18.10] Well, well, I've gotten through it alive and well. Hopefully
	 I'll be doing at least a little more work on HexIt in the
	 coming months. Time will tell. I probably shouldn't promise too
	 much. :) Heh, I'd better start writing those two first digits
	 of the year soon, lest this file crashes the next time you try
	 to read it! *gasp*

[ 18.20] CM: It was possible to assemble instructions in CodeMode even
	 when no file was loaded. The only time you can get that
	 situation is when you start HexIt without arguments and press
	 <Escape> at the "open file" prompt. Thanks Scid!

[ 18.30] CM: If no file was loaded, the screen wasn't updated after a
	 change of segment-size. It admittedly does little difference
	 since you can't edit anything without a loaded file, but it
	 still didn't look right.

[ 19.30] HM: Added a "Fill selection" checkbox to the InsertValue
	 function. Instead of inserting or overwriting data at the
	 current position, the currently selected block is filled when
	 this checkbox is true. If you've selected 9 bytes and decide to
	 fill the selection with dwords containing FEEDF00Dh, the last
	 byte is left untouched. Someone, I can't for the life of me
	 remember who it was, once suggested I add a function for NOPing
	 the selected block. That would be an excellent way of using
	 this new feature.

[ 19.40] CM: "rep" is now a valid synonym for "repe". I can't believe
	 this has gone unnoticed for such a long time. :-) Thanks go to
	 Jace and Scid.

[ 20.20] DM: HexIt would freeze (unless you were working on a really
	 small file) if you were in DumpMode, searched for something and
	 found it pretty far away from your starting point and then
	 tried to switch to CodeMode. Hopefully not many have been
	 harassed by this bug.

[ 21.30] CM: A rep-prefix followed by an instruction on the same line
	 assembles ok now.

[ 22.00] CM: What I mentioned two notes above this one about HexIt
	 freezing apparently applied to searches started in CodeMode as
	 well. If you tried searching from CodeMode and were happy
	 enough to find something, you'd have to wait quite a while to
	 actually see it. How long depended on how far the search had
	 moved the fileoffset.

[990311] After ml.org's death, and by that the death of the
[ 00.50] fluff.home.ml.org URL, I was left alone in the darkness with
	 noone to turn to. Suddenly emerged a sparkling dot. Out of that
	 brightly shining dot stepped Ubbe-Bubb and told me it was ok
	 for me to use http://octacom.net/fluff as a redirector to
	 whereever I may move. Right now that redirector points to my
	 ancient URL at geocities, but that will hopefully change fairly
	 soon. Just remember to use the octacom address and not anything
	 else.

[990324] CM: Assembling instructions in overwrite-mode didn't set the
[ 12.50] FileChanged flag. Credits to Angel Vidal.

[ 13.50] Pressing tab in a menu takes you to the next control now, as is
	 customary in UI:s.

[990521] Added an option in Setup->Screen->"Indiv. viewmodes for files?"
[ 21.10] that when set keeps a separate list of viewmodes for each file.
	 You'll then switch viewmode automagically when you switch file.
	 Sune Marcher is the reason this exists. Blame him if you don't
	 like an extra option. ;)

[ 21.40] Viewmode is now restored when exiting the helpfile.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.53 - 19 Nov 1998³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[981101] CM: Instructions with modr/m bytes of 0c0h or higher sometimes
[ 03.30] (_very_ rarely, it seems) caused a SIB byte to be output.

[981119] CM: Gosh, I introduced a spiffy little bug with v1.52. I hope
[ 21.30] you never tried to assemble memory operands with more than one
	 reg... Thanks a bunch to Sune Marcher for telling me!


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.52 - 16 Oct 1998³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[981002]  CM: "out 60h,al" could sometimes not be assembled twice in a
[ 16.30]  row due to a tiny, little bug in *gasp* The Expression Parser.

[981016]  CM: "aam" or "aad" without an immediate value is ok now and
[ 10.50]  automagically gets the proper 00ah second byte.

[ 11.00]  CM: "int 3" now uses the shorter CC form instead of CD03.

[ 11.40]  CM: You can use "imul reg,imm" instead of the syntactically
	  longer form "imul reg1,reg2,imm" when reg1 == reg2. Major
	  thanks to Sebastian Schuberth (aka Saint) for all his friendly
	  little emails. :-)

[ 14.30]  CM: "mov eax,[1234h]" from a 32-bit seg was assembled to
	  67A13412. I've changed this to A134120000 now.

[ 15.20]  CM: "[-1+bx]" was ok while "[bx-1]" was not (it was
	  interpreted like "[bx+1]". Sheesh.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.51 - 22 Sep 1998³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[980829]  HM: The value of the current byte is now shown in dec (both
[ 15.40]  signed and unsigned) on the statusbar.

[980829]  CalcIt: 1+(1+1)*2 is not often considered to equal 6. :) The
[ 22.20]  problem was related to parentheses. Added modulus operator.
	  Aah yes, *cough* I hope you never tried to divide anything by
	  zero... Good going, Fluff! *rofl*

[980830]  The cursor was behaving rather strangely on some ATI and S3
[ 00.30]  gfx cards. It was invisible in insert-mode and looked like a
	  typical insert-cursor in overwrite-mode. Trying to resize it
	  made no difference. Major thanks to Jeremy Chadwick (aka
	  Yoshi) for helping me out with this one! (P.S. For those of
	  you who might be interested: disabling alphanumeric cursor
	  emulation fixed the problem. Check out int 10h/12h, bl=34h)

[980906]  CM: "t."-prefixes looked rather strange. Thanks to mrz/ai for
[ 03.20]  telling me! (*laugh* I couldn't use an underscore in your nick
	  due to the fact that my htmlizer uses that char to denote
	  boldness. Sorry, chap. :-D )

[ 03.40]  CalcIt: Added an "Asc" field that displays the result like
	  ASCII characters.

[ 05.10]  CM: <Ctrl>+<CursUp>/<CursDown> didn't work correctly if you
	  were positioned on the last/first line on screen.

[ 11.50]  Removed date and time from the topmost row and replaced it
	  with info on how many bytes you've currently selected.

[980916]  CM: AzmIt only cared about the beginning of operands, i.e
[ 18.50]  "call di+2" and it's likes were ok.

[ 19.00]  CM: AzmIt sometimes ignored explicitly expressed operandsizes,
	  e.g "cmp b.[si],0".

[ 23.30]  CM: "[eax*4+eax]" didn't work. You can even write "[eax*5]"
	  now if you so prefer, although I can't for the life of me
	  imagine what sort of twisted person would write that... ;)

[980918]  Added a statusfield to CalcIt. "OK!" means no error was found.
[ 18.50]  Other msgs try to tell you what's wrong, you should listen to
	  them.

[ 21.00]  HM: New function: "Read block from file". Use <Ctrl>+<F4> to
	  access it. If you've selected a block, only that block will be
	  overwritten. Otherwise the loaded block will be inserted at
	  the current pos (overwriting existing bytes if Insert is
	  deactivated).

[980921]  CM: E6 42 was shown as "out   042  ; 'B',al". Thanks go to
[ 00.40]  Sebastian Schuberth (aka Saint)!

[ 23.40]  Added CalcIt and ReadBlockFromFile to the key-setup.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.50 - 27 Aug 1998³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[980326]  CM: Disassembling an instruction using the direct address
[ 20.30]  feature of a SIB byte fucked up one of my tables. This in turn
	  caused all following instructions w/ no offset at all to
	  disassemble as if they had a dword sized direct address
	  portion. Err... Aaah, well.

[980629]  CM: Just having bought myself a K6-2 processor, I figured it
[ 20.00]  would be rather embarrassing not to have support for 3DNow!
	  instructions... :)

[980712]  CM: Quite a lot of changes has been made to DazmIt (the
[ 23.10]  disassembling part of HexIt). Download the separate DazmIt
	  package and read the whatsnew file if you're interested.

[980713]  TM: Some things were not updated after a tabsize change. If
[ 21.00]  you went from 8 to 1, you'd probably see some funky stuff at
	  eof.

[980716]  Just a minor cosmetic fix; when pressing pagedown in the
[ 12.50]  "Global Keys" portion of the keysetup to go to page 2, the
	  current row wasn't displayed.

[980811]  "Ignore case" now defaults to on when searching in textmode
[ 15.40]  and off in all other modes.

[980819]  TM: A SIB-byte could be disassembled with esp as index-reg.
[ 14.00]  This is quite illegal.

[980827]  It seems HexIt could run into problems when trying to save a
[ 12.10]  file with the system-flag set. This may only apply to NT.

[980827]  HM: Pressing <Ctrl>+<F2> will prompt you for a filename and
[ 12.20]  offset and then write the selected block to the given file.

[980827]  CM: Pressing <tab> or <Ctrl>+<F4> (AzmIt) will allow you to
[ 12.30]  assemble an instruction! If Insert is active, the instruction
	  will, quite logically, be inserted into the bytestream.
	  Otherwise the old bytes will be overwritten.

[980827]  There, there, finally. Press <F9> to summon CalcIt. CalcIt is
[ 16.40]  an entity that thrives on the strange expressions you see fit
	  to feed him with. His excrements come in several different
	  flavors. Play with him and he will love you forever.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.40 - 22 Mar 1998³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[980222]  Added "-o OFFSET" to cmdline arguments. Use it to position the
[ 03.30]  cursor at a specified offset in the file. Remember that you
	  can use "-win WINDOWNUMBER" and "-file FILENUMBER" to specify
	  what window and/or file arguments have affect on. A cmdline
	  such as "hexit foo.com moo.com -o 64 -file 2 -win 2 -o 42"
	  would fire up hexit with two files loaded, foo.com and
	  moo.com. The cursor would be positioned at offset 64 in
	  foo.com and if you enabled splitscreen and displayed moo.com
	  in the bottom window, you'd find the cursor neatly positioned
	  at offset 42.

[ 05.40]  "hexit moo*" is now treated like "hexit moo*.*"

[980227]  Added functions for switching to specific viewmodes. Per
[ 20.00]  default <Alt>+<Fx> switches to viewmode x (TextMode = 1,
	  HexMode = 2, etc).

[ 21.00]  Added functions for switching to the previous/next viewmode.
	  Defaults are <Alt>+<CursLeft> and <Alt>+<CursRight>.

[ 22.20]  Added functions for storing and restoring (called Set/Get)
	  offsets. The "Set" version stores the current offset into a
	  specified area and the "Get" version restores that offset and
	  makes it the current one. There are 9 such areas to choose
	  from. They are, quite reluctantly, called 1-9. I accidentally
	  called them 0-8 on several occasions when writing them... :)
	  Considering their default keys, the names 1-9 make much more
	  sense though. Use <Alt>+<1-9> to Set and <Shift>+<Alt>+<1-9>
	  to Get.

[ 22.30]  Push and pop offsets onto/from a stack with default keys
	  <Alt>+<0> and <Shift>+<Alt>+<0>.

[980301]  Pressing <Home> or <End> in a string field in a menu didn't
[ 10.40]  set the fieldchanged flag. I.e if you pressed one of those
	  keys and then started typing, the field's old content would be
	  cleared.

[ 16.10]  CM: Added fxsave and fxrstor.

[980302]  The keystrokes <Alt>+<0-9> wasn't displayed correctly in the
[ 23.20]  keyconfig.

[980304]  The menus can now cope with checkboxes and hex textboxes. This
[ 01.30]  means I can rip out some really old code previously used to
	  draw the search menu.

[980310]  Changed the default color for unselecable items in menus from
[ 20.10]  gray to cyan.

[980315]  Well... It seems as if I've finally completed the search
[ 13.20]  routine xchg. Things should work a lot better now. The
	  possibility to search/replace backwards slipped in as well.

[ 20.40]  HM: Added big/little endian option to the InsertValue function
	  (<Ctrl>+<I>). Corrected a bug that occured when Size was 3.

[ 21.00]  CM: Configuring the bkg color was a rather hard thing to do.

[ 22.10]  If one of the files given on cmdline failed to load, HexIt
	  exited. Nowadays, HexIt fires up with the successfully loaded
	  files.

[980316]  Wow! Press <Ctrl>+<F8> to toggle macro recording and
[ 21.00]  <Ctrl>+<Enter> to play the recorded macro. Macros are limited
	  to 1024 keypresses.

[980317]  "-ss 1" on cmdline now puts the 2nd loaded file (if more than
[ 23.20]  1 file were loaded) in the 2nd window.

[980319]  CM: Each 66h (and 67h) prefix toggled the size instead of just
[ 20.50]  setting it to the opposite of the segmentsize. No, you're
	  right, a sane person would normally never have been bothered
	  by this. ;)

[ 21.30]  If you, for any reason, tried to run an earlier HexIt version
	  with a newer config file, HexIt crashed when trying to execute
	  functions that weren't implemented. This is fixed now. I
	  sometimes run earlier versions when trying to find out if a
	  bug, err... feature is newborn or if it's been living inside
	  HexIt for a while.

[ 22.00]  CM: Insanely long lines of hexbytes (probably due to multiple
	  66h/67h) no longer looks like abs(crap). Nor does it crash.

[980320]  TM: _FINALLY_ you can scroll the text left and right when
[ 20.30]  running in unwrapped mode. <Left> and <Right> are, quite
	  naturally, the default keys. By pressing <Ctrl>+<Left>/<Right>
	  it's possible to scroll the text X chars at a time where X is
	  the defined tabsize. *laugh* It was about time I fixed this...

[980321]  CM: Added MMX instructions. They seem to decode nicely, albeit
[ 18.20]  a bit slowly. Aah well, perhaps I'll get around to optimizing
	  DazmIt (my disassembly engine) someday.

[980322]  Added an option to, when starting HexIt with no arguments,
[ 22.00]  automagically create a new file called NEWFILE instead of
	  asking for a file to open. Config in Setup->Misc.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.32 - 15 Feb 1998³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[980214]  CM: The immediate data of 83f5ffh and it's likes is now
[ 20.30]  expanded to the size of the destination register.

[ 22.00]  CM: "b." etc wasn't displayed if the addressing mode involved
	  a SIB.

[ 23.10]  CM: The same goes for "push imm" instructions.

[980215]  HM: InsertValue (<Ctrl>+<I>) didn't set the FileChanged flag
[ 02.15]  properly.

[ 03.03]  Gave the replace-routine a much needed speedup.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.31 - 04 Jan 1998³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[971231]  CM: Added LIDT and LGDT. Thanks fly out to David Sicilia for
[ 04.50]  telling me!

[980103]  CM: If an instruction with a SIB contained no index-reg, it
[ 18.40]  was interpreted incorrectly. Thanks, SCaBBy!

[ 19.10]  CM: Searching/replacing didn't work very well.

[ 19.30]  CM: Made EXE-header available, <F6> is default key.

[ 20.30]  If a function was available from two or more modes, the
	  keyconfig would look a bit strange. It would include the
	  defined keys from all modes and not just the mode being
	  configured.

[ 20.40]  CM: Relative offsets were calculated from the start of the
	  instruction.

[980104]  CM: Displays preceding zeroes in addresses. E.g "mov ax,[0]"
[ 19.40]  is now "mov ax,[00000]" in 16-bit code. Blame SCaBBy. ;)

[ 20.00]  CM: If the last instruction in a file contains just one byte
	  of a two-byte opcode, you will now be positioned on the same
	  line when trying to move downwards.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.30 - 30 dec 1997³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[970914]  TM: Fixed a bug that occured if you had several files loaded
[ 20.30]  and decided to close a file. The displayed "Total Lines" in
	  the statusbar wasn't updated correctly. This one has been in
	  there ever since the possibility of closing files first
	  emerged, i.e v1.00.

[971002]  Creating files on write-protected disks didn't work very well.
[ 20.00]  It doesn't work now either but at least HexIt tells you so.

[ 20.10]  HexIt crashed if you tried to run it with no free mem (apart
	  from conv). This is thanks to a "fix" I made a _long_ time ago
	  where I subtracted 5 from the amount of free mem without
	  checking for carry, thus causing it to wrap around, reporting
	  4GB free mem...

[971004]  Some popups looked rather funny if you got to see them in
[ 15.30]  monkey-resolution splitscreen, i.e 80x25. Only parts of them
	  were displayed.

[ 16.30]  DM: Added "Fill-char" to the "Define Mask" function. As it's
	  name implies, it allows you to configure what character should
	  be used to fill masked areas.

[ 17.30]  It's now possible to configure "Initial viewmode" to DumpMode
	  or CodeMode as well as the pre-existing TextMode and HexMode.

[971005]  HM: When positioned in the textfield of the 2nd window in
[ 00.00]  HexMode, the cursor was placed one row too far down.

[971006]  GGGGGGGGNNNNNNNNNNNN!!! I've been tearing the hair off my head
[ 21.30]  for the last 3 hours! I was right in the middle of making some
	  cmdline-parameter routines when, to my big surprise, I noticed
	  that HexIt only used the first 9 arguments. Hmmm... Puzzling,
	  I thought. Could there be a problem with Tran's PMode? Did he
	  perhaps limit the cmdline to the first 9 args? I altered PMode
	  to display the contents of the cmdline immidiately upon
	  program-start. No? There _were_ only those 9 args! Hmmm...
	  What about 4dos then? Did 4dos have a flaw? Time for some
	  command.com *shiver*. Naah, still only 9 args! Wow! Cool! I've
	  discovered an undocumented anomaly of the cmdline! This
	  certainly goes into my "Notes" directory. This is when I sort
	  of happened to run CHKARG.COM and to my _huge_ surprise saw
	  that, indeed, there were more than 9 args there! Uuhu? Could
	  the problem be related to .exe-files only? A swift linking of
	  CHKARG.EXE proved me to be, once more, utterly wrong. Gosh!
	  Alter PMode again, just to be sure... Naah, still no change.
	  Hummm... What am I doing differently when running
	  "h 1 2 3 4 5 6 7 8 9 0 1 2" compared to
	  "chkarg 1 2 3 4 5 6 7 8 9 0 1 2" ? *think*, *think* hmm...
	  NOOOOOOOOOOOOO!!!!!!!! "h" is in fact a .bat-file I've made
	  that runs "hexit.exe %1 %2 %3 %4 %5 %6 %7 %8 %9"! SHEEESH!!!
	  I think I'll spend the evening writing "%&" a couple of
	  times...

[ 22.00]  Pheeew... Ok, the cmdline-stuff seem to work fine now. Here's
	  what you can do:
		"-vm X"         ; viewmode (1=TextMode, 2=HexMode, etc.)
		"-file X"       ; file that args affect (1=first)
		"-win X"        ; window that args affect (1=first)
		"-ss X"         ; splitscreen (0=off, 1=on)
		"--"            ; interpret the rest as filenames
	  "win" and "file" both defaults to 1.
	  "hexit hexit.exe -vm 3 -win 2 -vm 2 -ss 1 -- -gnu" would start
	  HexIt in SplitScreen, DumpMode in the upper window and HexMode
	  in the lower with two files loaded "hexit.exe" and "-gnu".

[971126]  HM: The pasted block gets selected _now_ (even if you're not
[ 21.10]  pasting to the file you copied it from.)

[971201]  CM: Added 'foof' instruction. Try running F00FC7C8 if you're
[ 01.00]  feeling bored.

[ 02.10]  CM: Fixed yet another bug that caused the disasm to crash (in
	  a most evil kind of way).

[971202]  Added "Yes, all" and "No, none" to the "Save changes?" popup.
[ 01.40]  These options save all or none of the changed files.

[ 02.40]  If you're running low on memory and the clipboard will have to
	  be truncated in order to be able to load a file, HexIt now
	  gives you an option to cancel the loading.

[ 21.50]  CM: <Ctrl>+<F2> toggles between 16- and 32-bit code.

[971221]  CM: Fixed a slight bug that caused the cursor to flicker and
[ 00.20]  pop up damn nigh everywhere on the screen when moving through
	  a file.

[ 01.30]  CM: Added functions for moving left/right.

[ 02.00]  CM: NibbleMove affects CodeMode as well as HexMode now. The
	  state of the NibbleMove flag as well as the current
	  segment-size is displayed on the Statusrow.

[ 03.50]  CM: Killed some more bugs in the move-routines.

[971222]  CM: Removed support for some non-existing instructions.
[ 03.40]  "call d.dx" doesn't really make sense, does it? ;)

[ 05.20]  CM: *cough* Readded support for "call d.[bx]" which, on the
	  contrary, _do_ exist!

[ 06.10]  CM: Imagine the bytes b8123456 at the end of a 32-bit code
	  stream. They're all shown on one line now, despite the fact
	  that there's still bytes (one byte in this case) missing.

[971225]  CM: Aah, xmas is over, sort of... Anyways, when you move past
[ 22.40]  eof and the last instruction is not complete, e.g "b800",
	  you'll now end up on the same line as the last instruction
	  instead of on the following one. This makes much more sense,
	  believe me.

[971226]  CM: Your offset into the current instruction is saved when you
[ 01.00]  move up/down.

[ 04.20]  CM: ___MAJOR___ speed increase when moving upwards in a file!
	  Added <PageUp>/<PageDown>.

[ 05.40]  CM: Added functions for decreasing/increasing screenoffset,
	  <Ctrl>+<CursLeft>/<CursRight> by default. Added scrolling
	  up/down one line, <Ctrl>+<CursUp>/<CursDown> by default. Added
	  moving to bof/eof, <Home>/<End> by default. All these
	  functions behave very similarly to those found in HexMode.

[971228]  HexIt now works fine under NT (again). I just can't seem to
[ 16.10]  let go of negative offsets... Sheesh! Will someone please
	  spank me?

[ 17.00]  CM: Fixed a silly bug that caused HexIt to crash occasionally
	  when walking upwards in strange codestreams. The reason? HexIt
	  would go berserk and start reading from far-away places. It
	  was quite amusing to see that windows 9x didn't care much, it
	  didn't even notice. Duh!

[ 23.30]  CM: Added <Ctrl>+<PageUp>/<PageDown>.

[971229]  HM: Backspace has gotten a tiny mind-boost. It now behaves
[ 00.10]  differently depending on your current NibbleMove status.

[ 00.20]  CM: Added <Delete> and <BackSpace>. They behave pretty much
	  like they do in HexMode.

[ 02.00]  DM: Any offset was valid in Goto!

[ 02.10]  CM: Added Goto, <F5> is default key.

[ 02.20]  CM: Switching file no longer positions the cursor at the
	  topmost line.

[ 03.10]  CodeMode functions were available from _all_ modes!

[ 05.50]  Added configuration options for CodeMode's keys and colors. If
	  you haven't changed the keybindings, you'll enter Setup by
	  pressing <Ctrl>+<F9>. I took the opportunity to add some more
	  colors to CodeMode. You can now define separate colors for
	  active and inactive lines.

[ 06.00]  A minor cosmetic fix concerning the "save config?" question
	  you get when exiting HexIt with unsaved, changed files.

[ 06.30]  Added config for CodeMode's default segment size. Look under
	  Setup->Miscellaneous.

[ 06.40]  CM: Fixed yet another cosmetic flaw, this one appeared when
	  you moved upwards and were positioned on the topmost line on
	  the screen.

[ 19.30]  CM: Added comments when instructions involves immediate data.
	  You can choose from 3 comment modes, "None", "Some" and "All".
	  "None" never shows any comments. "Some" shows comments if the
	  instructions is MOV, ADD, SUB, PUSH or CMOV. "All" always
	  shows comments when immediate data is involved. You can select
	  default comment mode in Setup->Miscellaneous.

[ 20.30]  Performed a much-needed update of HEXIT.DOC...

[ 20.40]  CM: When the last instruction was incomplete and it was the
	  only one on screen, you couldn't press <CursDown> to get to
	  the end of that instruction.

[971230]  CM: Comments now have their own colors. Feel free to set them
[ 02.40]  to the color of instructions though...

[ 03.40]  CM: The immed data in an INT is _never_ commented now. That's
	  just silly.

[ 05.20]  Added config options for the background character in
	  menufields ('°') and the cursorsize in numerical menufields.
	  You can find these options as well as many other under
	  Setup->Miscellaneous.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.20 - 13 sep 1997³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[970909]  Oops, I forgot to mask away the high nibble of AL from INT
[ 00.50]  16h,2h in one place. Therefore, pressing Insert, CapsLock,
	  NumLock or ScrLock affected the appearance of the keybar.

[970911]  When the "Helpfile not found!" popup was displayed, the cursor
[ 18.20]  wasn't hidden.

[ 19.20]  The Statusrow in HexMode now displays a little '1/2'-sign if
	  NibbleMove is activated.

[ 20.30]  When running SplitScreen and typing in one window (HexMode),
	  the other window now gets updated as well.

[970913]  I've now added a new mode, DumpMode. It's pretty much like the
[ 10.40]  TextMode, with a few exceptions, notably:
		Linefeeds and tabs are not parsed
		There's an address-field on the left side of the screen
		You can define and use a mask, <Alt>+<M>
	  Toggle the mask on/off by pressing <Ctrl>+<M>. The mask-popup
	  consists of three fields:
		"Repetitions": Min # of passed bytes req for visibility
		"Lower limit": All bytes below this value are masked off
		"Upper limit": All bytes above this value are masked off
	  Look in Setup->Misc and Setup->"DumpMode colors" for
	  configuration options.

[ 13.10]  Changes in default keys:
		Removed <Ctrl>+<G> and <Ctrl>+<J>
		<F5> is Goto in all modes
		<F2> is Save in all modes
		<W> wraps/unwraps text in TextMode

[ 13.30]  The key to bring up "Setup Keys" wasn't configurable.

[ 13.50]  HexIt crashed if you had no files loaded, was in HexMode with
	  InsertMode on and started entering text.

[ 14.30]  The "Change filename"-popup didn't work very well from time to
	  time... There were 2 bugs, including one in my general
	  menu-string-item routine.

[ 17.40]  Change the tabsize by pressing <Ctrl>+<F2> in TextMode.
	  Default size can be set in Setup->Misc.

[ 18.20]  It's now possible to compare a file with itself. *Sniff* No
	  more headaches... ;)


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.13 - 04 sep 1997³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[970830]  It's now possible to select bytes (in hexmode) by pressing and
[ 21.10]  holding the <Shift>-key while moving the cursor. Note that if
	  mark1 equals mark2 then the selection is cancelled. If you
	  want to select just one byte, use <Alt>+<A>.

[ 21.20]  Ok, I've removed all swedish docs now! Having to update one
	  doc is quite enough for me. And besides, computers were not
	  meant to be bothered by any other languages than asm and
	  english. You say you don't speak english? Obviously, you do.

[ 22.00]  When pasting, the pasted block now gets selected.

[970831]  Added <Shift>+<Del>, <Ctrl>+<Ins> and <Shift>+<Ins> to the
[ 00.40]  default set of keys. You know what they do.

[ 01.00]  If you tried to cut or copy and didn't have enough free mem,
	  HexIt wouldn't tell you so... Now he (that's Mr. HexIt) does.

[ 03.03]  <Ctrl>+<I> now brings up a menu allowing you to insert a value
	  at the current position. Just answer these questions:
		What value should be inserted?
		How many bytes long is the value?
		How many times do you want to insert the value?
	  As usual, remember that the base can be toggled with
	  <Ctrl>+<Tab>. If InsertMode is on, the rest of the file will
	  be pushed forward, otherwise things will be overwritten.

[ 13.00]  <Alt>+<K> now pops up the "Setup Keys" menu. This is
	  (methinks) a great way to find out what keys to press in order
	  to activate certain functions.
	  Been around for a while? Miss the old keyhelp on <Alt>+<H>?
	  Then this is for you.

[ 13.50]  If you defined an "unknown" key as "first keypress" in the
	  KeySetup, HexIt didn't show the 2nd key.

[ 15.30]  When pasting in OverwriteMode and the pasted block stretches
	  beyond EOF, you'll now be asked if you want to expand the
	  file.

[ 20.00]  Aah, yes! The KeyBar at the bottom of the screen now
	  interprets your current key-config and displays the correct
	  functionnames accordingly!

[ 20.30]  You'll now be prompted to confirm when trying to define a key
	  that's already been defined.

[970904]  Search/replace always started at the current position+1. It
[ 19.50]  only does that now if a previous search/replace found a match
	  at the current position.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.12 - 24 aug 1997³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[970824]  HexIt crashed when exiting the setup if you'd entered the
[ 16.00]  keysetup.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.11 - 19 aug 1997³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[970724]  I finally split hexit.asm into several smaller files! I would
[ 21.30]  have _had_ to do that soon, 'cause the assembler was starting
	  run out of memory when assembling... :) Not that this concerns
	  you in any way, I just thought you'd be interested? *cough*

[970729]  When closing the help-file (by pressing <Alt>+<H> once more),
[ 18.30]  HexIt didn't close the helpfile. It closed the current file
	  instead... :)

[970730]  The URL to HexIt's homepage has changed. From now on,
[ 23.00]  http://fluff.home.ml.org is where you _want_ to go today.

[ 23.30]  Wow! It struck me right now that the new <Alt>+<H> helpsystem
	  is really cool! =) Looking up keys has never been easier, just
	  search for the abbreviation! I.e, press <F7> and enter "^F1"
	  if you're interested in the <Ctrl>+<F1> key. Or... you could
	  have searched for "videomode" if you'd forgotten the key. This
	  method will of course only work if you use the standard
	  keybindings. But on the other hand, if you've changed it,
	  you've probably changed it to something that's easier for you
	  to remember... ;)

[970802]  Ouch... With NibbleMove activated you'd always move only one
[ 13.00]  nibble when pressing <CursLeft>/<CursRight>, even if you were
	  positioned in the textfield.

[ 13.30]  You can now toggle NibbleMove by pressing <Ctrl>+<N>

[970807]  *cough* HexIt v1.10 used to crash under NT 4.0 (perhaps under
[ 12.00]  other versions as well). It works fine now, although I have no
	  idea why... Oh well, it works! ;)

[ 17.50]  Filenames can now start with a dash ('-'). (Thanks Andr‚s!)

[970816]  I removed the "Loading HexIt vX.XX, please wait..." msg. Why?
[ 14.40]  Why not?

[ 16.00]  Updated the docs a bit...

[970817]  Previously when pressing <F3> to choose a file, the next file
[ 13.20]  was the default option. Now, the current file is default.

[ 13.40]  When choosing "Default configuration" from the mainmenu of the
	  setup, HexIt zeroed the HexIt-Counter (tm) as well. No more!

[970818]  _Finally_ you can configure your own keybindings! There are
[ 18.00]  two keys that can neither be changed nor removed though:
		<Ctrl>+<Alt>+<BackSpace> = Exit
		<Ctrl>+<Alt>+<Enter> = Setup
	  These exists just to make sure you don't f*ck up completely...
	  You can have as many as 5 different keys for any one function.
	  If you need more, you prolly should've left that last beer
	  alone.

[ 18.10]  When you entered a submenu from setup->misc, your chosen
	  option in setup->misc was reset to the uppermost one. Err,
	  what this means is that if you pressed enter over e.g
	  setup->misc->"wrap lines as default?", you'd find yourself
	  positioned over "start in overwrite- or insert-mode?" when you
	  came back to setup->misc... Ok, ok, nevermind then! ;)

[ 19.30]  Instead of giving a cryptic (to some people) help-msg when
	  running just "HexIt" or "HexIt /?", HexIt now starts up and
	  prompts you for a file to load. I do hope all HexIteers will
	  be able to figure out what to do now...

[970819]  *laugh* Remember what I said about closing the helpfile
[ 19.20]  actually closed the active file in HexIt v1.10? There was
	  another bug involved as well. Any additional files you had
	  loaded after the helpfile (or rather, the active file) except
	  for the one directly following it wasn't correctly preserved
	  when you closed the "helpfile".

[ 21.20]  I made a little change in the way IncScreenoffset and
	  DecScreenoffset work. It's now possible to increase your
	  screenoffset even if the entire file fits on screen.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.10 - 23 jul 1997³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[961222]  Added <Ctrl>+<J> as [GoTo] in hexmode. Btw, those of you who
[ 16.30]  don't read the docs might want to know that you can prefix the
	  value with a plus- or minus-sign to move relative to the
	  current position... ;)

[961223]  Numerical menufields didn't show the base-character ('d' or
[ 16.00]  'h') if you weren't standing in the field. (Thanks Funnel!)

[961228]  When closing files, the "File has been altered"-popupmenu was
[ 12.40]  always displayed, no matter if you actually had altered it or
	  not!

[961230]  When pressing <Home> HexIt SHOULD have crashed! It only
[ 21.00]  crashed sometimes though... err, well, it's fixed now! :)

[970722]  HexIt always initialized the videomode when you started/exited
[ 16.10]  it. Thus if you had a crappy monitor (like I do) you'd have to
	  wait 5 secs or so for the monitor to switch mode... duh! Now
	  if the requested mode is already set, HexIt just clears the
	  screen.

[ 16.20]  *smile* A friend suggested that I should write something nicer
	  than "Damnit, register!" when exiting an unregistered HexIt.
	  You've never seen that sentence? Good... ;)

[ 17.20]  Just a fun little thing... When you exit HexIt you'll now see
	  how many times you've run it.

[ 20.00]  Not a feature exactly, but anyway... I've started using a
	  build-number just to show you guys how much hard work I put
	  into HexIt! ;) It's probably way to low, but don't worry...
	  It'll soon be pretty high anyway! *g*

[ 22.00]  Due to various magic features, HexIt was sometimes not able to
	  read (nor write) the configfile...
	  The infamous "Error: Couldn't open file!" has met it's
	  destiny! ;)

[ 22.20]  If you were positioned at the first byte (but over the low
	  nibble) and pressed <CursLeft>, you didn't get to the high
	  nibble of the first byte.

[ 22.50]  Previously you always moved to the prev/next byte when you
	  pressed <CursLeft>/<CursRight> in the hex-field in hexmode.
	  I've now added an option that enables moving from nibble to
	  nibble instead. This feature (like many other) was suggested
	  by Andr‚s Mazzocchi, huge thanks fly out to him!

[ 23.20]  I've enabled background colors 8 to 15 now. See comment above
	  for credits... ;)

[970723]  In earlier versions when you were editing a hexfield in a
[ 00.00]  popupmenu, all letters from A-Z were allowed! Ooops... ;)

[ 00.50]  A setup-option for selecting default base in numerical
	  menufields. Note that the default base doesn't apply to all
	  fields, there are some cases where that would be quite useless
	  and stupid. (You can still change the base in those fields if
	  you press <Ctrl>+<Tab>)

[ 02.20]  <Ctrl>+<G> works exactly the same way <Ctrl>+<J> does. Thank
	  Scid for that... *growl* ;) Oh well, I suppose I'd better make
	  a keyconfig someday.

[ 05.00]  Added configuration-options for changing the colors in the new
	  menus.

[ 05.50]  Aaaaah... Yes! HexIt is once again FREEWARE! Use it 'til your
	  heart bursts! This means you get all the snazzy features that
	  only the registered versions had earlier, i.e loading of more
	  than 1 file simultaneously... ;)

[ 07.30]  I've removed the previous keyhelp-section. Now when you press
	  <Alt>+<H>, HexIt loads the doc-file HEXIT.DOC from HexIt's
	  home-directory and displays it in the current window. Note
	  that this makes it possible to split the screen and have the
	  helpfile loaded in one of the windows... Be sure to put the
	  docfile(s) in the same dir as the executable.

[ 16.40]  Fixed a bug when changing filenames with <Ctrl>+<K>+<R>. If
	  you pressed <Escape> the screen wasn't updated correctly.

[ 21.00]  Added a configuration option for choosing help language. Only
	  English and Swedish are available though.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v1.00 - 21 dec 1996³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[960709]  The keybar (bottomrow) now gets emptied whenever you popup a
[ 18.10]  menu if all functionkeys are "dead". Previously you could be
	  fooled into believing that pressing F1 in the Setup-menu would
	  let you switch videomode.

[960714]  In hexmode, Ctrl+CursLeft/Right now decreases/increases your
[ 02.25]  baseaddress (address of the first byte shown on screen).

[ 17.10]  The filename is now shown correctly on the statusrow even
	  under windows95!

[ 19.30]  The binary value of the byte you're positioned over is
	  displayed on the statusrow (hexmode only).

[ 20.35]  Upgraded from PMODE 2.50 to PMODE 2.51. If there is a later
	  version, please contact me!

[ 21.00]  If you were positioned after the last byte in a file and
	  pressed <Del>, HexIt acted as if you'd pressed <BackSpace>.

[ 21.00]  If you pressed Ctrl+PgDown in hexmode and were less than 1024
	  bytes from the eof, HexIt would position you at the last byte
	  in the file, not one byte after the last as it should. (Also
	  fixed a similar bug in Goto)

[960715]  Added a new displaymode: 80x60.
[ 16.00]

[960721]  After a night with no sleep I feel like a new man again... ;)
[ 09.30]  Anyway, HexIt now tells you exactly how much more lo mem you
	  need if you have too little to start HexIt. I think earlier
	  versions of HexIt would have acted kind of strange if that
	  occured, probably ignoring it and using whatever block in mem
	  it happened to feel like.

[960804]  If autodetecting startup-videomode, your mode was not marked
[ 04.50]  as default when pressing Ctrl+F1.

[960909]  A friend of mine figured out how to use external viewers in NC
[ 23.20]  5.0! Almost at the bottom of the file, you can normally read:
		~wpview.exe
		$*.exe,p
		$*.com,p
		$*.dll,p
		$*.*,p
	  or something similar. Comment that out by preceding each line
	  with a # character. Now add this instead:
		~hexit.exe
		$*.*,e

[960916]  I leaped one step closer to full pathnames on cd-roms. You'll
[ 17.00]  see everything but the driveletter now.

[960917]  "HexIt f:gnu.asm" works fine now. It loads the file "gnu.asm"
[ 12.30]  from the current directory on drive F. Previously HexIt tried
	  to load the file from the current directory on the current
	  drive.

[ 12.50]  "\.\" in the path is now correctly translated to "\". Any
	  number of dots in the path is also translated to the correct
	  number of parent dirs, e.g if your current directory is
	  "c:\dos\tmp\fluff\" and you run "HexIt ....\msdos.sys", the
	  path is translated to "C:\MSDOS.SYS".

[961119]  When using HexIt as viewer in NC, you could not view files
[ 11.40]  with filenames consisting of only one character.

[961120]  If you created a new file and then pressed F4 a couple of
[ 13.30]  times, HexIt crashed. (Thanks Funnel!)

[ 22.00]  Created files were marked "changed" from scratch. I've changed
	  my chaotic mind about this now... ( Seeing "Save changes?"
	  every time I run "hexit tmp.com" to test new features is
	  starting to annoy me... ;) )

[961129]  Aaaah! Finally my new menusystem is working well enough to be
[ 19.30]  usable! This means things will start rolling again...

[ 19.40]  To jump to a specific line in textmode, just press Ctrl+J and
	  enter the linenumber.

[961130]  If HexIt takes long time to start up, you might want to change
[ 01.30]  your mousedriver! Some drivers take several seconds to
	  initialize while others are real smooth. It really shouldn't
	  take *any* time, so try to find a nice driver, will you?

[ 01.50]  If you were positioned after the last byte in a file and tried
	  to search or replace, HexIt would search 4GB of mem... ;)

[ 14.30]  Pressing Ctrl+C to compare again automagically changes
	  compare-mode to "Forward from current position" if you have
	  previously compared "From file-beginnings" and to "Backward
	  from current position" if compare-mode previously was "From
	  file-endings".

[ 14.50]  When searching, HexIt displays a little sign saying
	  "Searching...". This simply tells you HexIt hasn't died... :)

[ 15.10]  Ctrl+A now marks the entire file. Note that this only applies
	  to hexmode.

[ 16.50]  If you choose to "Replace all", you can now break out of the
	  replace-routine by pressing <Escape>. This is useful if you
	  accidentally chose to replace all zeroes in a 42MB big file
	  consisting only of zeroes and you don't wanna wait til the end
	  of the world to continue using HexIt... ;)

[961201]  HexIt would sometimes crash if you tried to cut... (it's too
[ 03.20]  late to jump into details! ;) ) Major thanks to Mikeee for
	  telling me!

[ 04.00]  Killed another bug! This one was a remnant from a time of
	  innocence, a time when I had not yet heard of page faults...
	  December is promising to be a good month! ;) The bug appeared
	  in the shape of a big, terrifying, child-eating Crash if you
	  tried to compare 2 files and your offset in the first one
	  (after comparing) could not be used as a ptr to read bytes
	  from... <giggle>

[ 20.10]  The path "f:gnu.asm" previously only worked if it was the
	  first argument.

[961204]  HexIt now displays a "Comparing..."-msg while he is comparing
[ 17.00]  your files.

[961218]  Pressing F6 in hexmode now displays the exeheader. You can
[ 22.20]  then read/write, calculate and goto different places...

[961219]  In the jump-to-a-line dialog, you can precede the number with
[ 20.00]  a minus or a plus to jump up/down X lines.

[961220]  YES! You can now load files from within HexIt! Press Ctrl+K
[ 18.50]  followed by 'O' to bring up the "OpenFile"-menu. From now on I
	  will write these key-combinations like this: Ctrl+K+O

[961221]  Quit files with Ctrl+K+Q.
[ 10.00]

[ 18.05]  Goto line (just as Ctrl+J) by pressing Ctrl+K+L. (Added on
	  request)

[ 18.10]  Change path and filename with Ctrl+K+R.

[ 20.00]  GotoOffset in hexmode (F5) now allows you to offset from
	  current position by preceding the number with a plus or minus.

[ 20.50]  When entering numbers in menufields, you can toggle base
	  between dec and hex by pressing Ctrl+Tab.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.99 - 11 jun 1996³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
[960402]  This listing will from now on include the current time and
[ 18.15]  date when I coded the feature (Dates are YYMMDD, times are
	  24-hour CET).

[ 18.15]  I decided to skip the BETA in the versionnumber. I think HexIt
	  works really well now.

[ 19.15]  Added mousesupport in textmode! You can now scroll the text up
	  and down by moving your mouse up/down. Customize your speed in
	  the setup-menu. (Ctrl+F9)

[ 23.05]  It is now possible to make use of your mousebuttons as well!
	  You can eg use left mousebutton to toggle wrap/unwrap, right
	  button to switch linefeed-characters and middle-button to
	  bring up help on keys. There are quite a few possible ways of
	  defining your buttons, check them out in the setup-menu.

[ 23.10]  When pressing <Esc> from within the searchfunction in
	  textmode, the cursor didn't disappear.

[960403]  Added mousesupport in hexmode too. As usual, customize your
[ 19.25]  settings in the setup-menu.

[ 21.05]  The search- and replacefields were a bit buggy when it came to
	  nibbles...

[960413]  Dropping one block-marker is now enough. I thought it a waste
[ 01.50]  of time having to press Alt+A a second time... :) Of course,
	  you still CAN press it twice if it makes you feel good.

[ 02.10]  When comparing files, HexIt didn't stop at the end of the
	  smallest file, but instead at the end of the largest one, thus
	  moving the indexpointer to a galaxy far, far away...

[ 02.35]  Zerolength files had one major drawback, if you had loaded a
	  file after the one with zero length, you automagically
	  thrashed the contents of the last file when inserting bytes in
	  the previous one... Eeh, am I losing you? I sure feel pretty
	  lost myself... ;)

[960420]  When first entering HexIt and pressing F4, your current mode
[ 17.40]  should be selectable as default. This however, was not the
	  case when using textmode as startup-mode.

[960515]  For some reason, I can not utilize the five last bytes of
[ 21.55]  available memory. HexIt crashes with a page fault error if
	  trying to do so. Anyhow, this is easily fixed, right? I just
	  reduce your available amount of mem by 5 bytes! Try not to cry
	  too much about all that lost mem... Who said cheap? ;)

[960516]  I've changed a detail concerning the way filecomparing works.
[ 13.05]  When comparing "from current pos", HexIt now starts comparing
	  the bytes following the current ones. This means you can now
	  easily compare multiple times in a row and find new
	  similarities/differences instead of having to move your
	  position manually between each compare. Btw, HexIt used to
	  crash if you were positioned on the second byte in a file and
	  tried to compare "backwards from current pos".

[ 16.30]  If you've changed your configuration and try to exit without
	  having saved it, HexIt will ask you to confirm.

[ 17.20]  I've recoded my routines for the <End> and <Home> keys. You no
	  longer have to wait several seconds after pressing one of
	  those in i REALLY big file.

[ 18.00]  If you gave a nonexisting filename as first argument, HexIt
	  would create it no matter if you decided to save it or not.

[960517]  Aah, finally it's possible to use wildcards when loading
[ 13.10]  files! Both '*' and '?' are ok.

[ 13.25]  The percent-number on the statusrow in textmode now shows 100%
	  if you can see the last row on screen. Previously you would
	  have to be positioned on the last row.

[ 14.00]  I changed the maximum number of files from 50 to 100. I needed
	  to edit 92 files simultaneously... :) Btw, if you need more
	  than 100 files, just send me a mess and I'll fix it, okay?

[ 14.20]  You can now press Ctrl+C to compare again with the same
	  settings as the last time. If you have not previously selected
	  comparemode (by pressing Ctrl+F3), you will be prompted to do
	  so.

[960611]  It's now possible to register by PostGiro.
[ 00.00]


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.98á - 24 mar 1996³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ Ok, at the very bottom of the screen there is now help concerning the
  functionkeys. It updates as you press Ctrl or Alt and will thus always
  contain the right help.

+ HexIt now has it's own homepage!
  Check out http://www.geocities.com/SiliconValley/3642 to obtain the
  latest version!

+ I have finally understood how Norton Commander passes argument to the
  viewer... Or, more appropriately, it works now. It's done in a VERY
  strange way! Anyhow, you can now use HexIt as your NC-viewer. I do! ;)

+ Esc now exits HexIt. I found this to be very convenient when using
  HexIt as a normal text-viewer...

+ A row at the very top of the screen displaying date, time,
  versionnumber, insert- or overwrite-mode and available mem.

+ Ctrl+CursUp/Down now takes you 16 bytes Up/Down just like the usual
  Cursorkeys do but the screen will scroll instead of the cursor! Thus
  you will stay on the same row on screen while the bytes in the
  background glide past you... If you're familiar with QEdit (great
  editor!) you'll know what I mean (perhaps). I've really missed this
  feature!

+ It sure is a LOT easier to customize your colors now! Everything is
  done from within HexIt, thus you can see your changes take effect
  immidiately! I've also added some extra stuff that can be configured,
  just check it out and see for yourself. Of course, you can still use a
  cfg-file from an earlier version. Just load HexIt as usual, alter
  whatever you want and then save it to upgrade your cfg-file! Oh yeah,
  press CTRL+F9 to enter setup-mode... (I've removed the old "/S" option
  on the commandline)

+ ALT+P now works exactly the way ALT+N doesn't! ;) That is, it starts
  editing the previous file in the list of loaded ones.

+ Finally I've coded the filecompare-routine! Press Ctrl+F3 to use it.

+ Introduced a popupmenu where you select which file you want to edit
  (among the ones already loaded). Pop it up by pressing F3.

+ You can now create new files simply by giving the filename as an
  argument. You will then automagically be prompted to save when
  quitting, no matter if you've written anything in it or not.

+ It is now possible to go one byte beyond EOF. This makes it possible
  to edit files of zero bytes length. It also gives you the possibility
  to insert bytes AFTER the original file. Previously you could not go
  beyond the last byte of the file...

* If you had been fluffing around with your configfile and made it
  larger than the one HexIt produces, you would always get the sligthly
  annoying msg "Your configfile seems to be corrupted!". Of course, you
  could just delete it. But then again, deleting IS hard, isn't it? ;)

* Aaah... Lovely! The textviewing works much better now, even with
  binary files. I won't even bother to describe all the changes 'cause
  the textviewing REALLY sucked earlier!

* The cursor didn't look very good in insert-mode when using 80x25 or
  80x28. (I hadn't noticed because I dont like those modes... ;)

* After dropping a marker in the file foo.dat you could drop the other
  in bar.dat, thus creating a block stretching over two (possibly more)
  files... This was not good! So, a block can only exist in one file at
  a time now.

* Improved helpsystem. I removed the key-help from F1 and introduced
  ALT+H which brings up a screen with lots of info about all possible
  keys. Note that F1 is still there, it just doesn't give any info on
  the keys anymore.

* After pressing F4 (or CTRL+F1 for that matter), HexIt didn't exit the
  menu if you pressed <Esc>. I also removed the "ESC: Exit
  helpfunction"-msg in the helpsystem. <Esc> still exits though.

* The cut-routine was pretty buggy earlier, the system would sometimes
  lock up if you tried to cut away the last byte in a file. This should
  be fixed now.

* The way I spend my evenings! I've removed most of the mudding and
  replaced it with some good ol' coding... ;)


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.97á - 20 nov 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ Added a textviewing mode! Press F4 to choose which mode to view the
  file in, text or hex. It doesn't look very nice if you try the
  textmode on binaryfiles though... That, however, will soon be fixed!

+ Added a swedish documentation.

* HexIt didn't exit if you chose to save changes when pressing ALT+X.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.96á - 07 oct 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ There is now an online helpsystem just a keypress away.

+ Added Ctrl+PgUp/PgDown. These keys take you 1024 bytes up/down in the
  file.

* I introduced a new bug in HexIt 0.94á, that once again caused it to
  crash with OS/2 v2.1. I can't seem to let go of negative offsets...
  Anyway, this is fixed now.

* Fixed even more 'bugs' with the filehandling. DOS doesn't break in and
  say "Trying to write on a write-protected disk!" every time you do so.
  Instead, HexIt does that! :)


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.95á - 03 oct 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ It wasn't possible to edit files on a CD-ROM before. Read more about
  it in HEXIT.DOC. You still can't save them though... :)

+ Added support for 28 and 43 rows videomodes.

+ The Search and Replace functions now store your last used field. If
  you, e.g were writing in the S-HEX field, then you will automatically
  be positioned there the next time you enter Search/Replace.

* The "Replace this?"-window used to be able to pop up on the wrong part
  of the screen if you were running splitscreen.

* Oops, pressing F4 popped up a menu saying "Save changes?"... That was
  part of my testing... :)

* Just a minor thing, when getting the message "Read-only file!", you
  were given two options, "Save anyway!" and "Don't save changes!". The
  hotkeys for those two options were 'Y' and 'N', that just doesn't seem
  right now, does it? The hotkeys are now 'S' and 'D'.
  There's one more thing to this subject, if you chose "Save anyway!",
  and tried to write on a write-protected disk, HexIt didn't notify you,
  it just acted as if it really did save the file.

* In some popupmenus, the cursor wasn't hidden, and after some others it
  wasn't restored to it's correct state.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.94á - 23 sep 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ The setup-mode now writes to a separate file instead of directly to
  the exefile. This has one major advantage, it is now possible to
  crunch HEXIT.EXE with an exe-cruncher, e.g LZEXE. Read more about it
  in HEXIT.DOC.

+ Added replace-routines, some modifications to the search-routines was
  all there was to it. Due to my tired brain, it still took some time
  though...

* Eliminated a bug in the search-menu that caused the cursor to position
  itself far too much to the right if you had previously typed in a
  search-string longer than 22 bytes. Eeh, you understand what I mean,
  don't you? X-)

* HexIt used to refuse to open write-protected files. Now you just open
  them as you would open any file, but you are prompted to confirm when
  trying to save them.

* I changed the way BackSpace acts in the hexfield.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.93á - 10 sep 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ Added search-routines, read more about it in HEXIT.DOC.

* A bug caused the screen to get only partially cleared when pressing
  ALT+X if you were running splitscreen and the first changed file was
  shorter than half the screen... Are you with me? :)


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.92á - 05 sep 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ Added a Goto-routine, simply press F5 and start inputting the address
  in hex.

* A bug appeared in v0.91á, it caused the last row's textfield to look a
  bit strange.

* HexIt 0.90á and 0.91á caused a crash under OS/2 v2.x, hopefully I have
  fixed this now. I can't tell, since I don't own that version of OS/2.
  I think it is fixed however. I used negative offsets in one place, and
  OS/2 2.x doesn't like that very much obviously... :) It seems to work
  well under Warp though.

* There aren't 1KB of zero-bytes at the end of HEXIT.EXE anymore.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.91á - 03 sep 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
* The setup-mode caused a total crash in 0.90á if you tried to save the
  changes. And besides, you couldn't even edit all the colors in that
  version.

* Pressing Esc doesn't bring up any non-working menus any more, you'll
  just have to wait, menus are coming soon.

* Now I've removed the final ounce of flicker. Previously it flickered a
  lot e.g when switching from/to splitscreen.

* Marked blocks now look a bit better in the hex-field.

* HexIt would crash if trying to load a zerolength file, now it simply
  refuses to load it.

* The "filechanged"-marker didn't update correctly when pasting.

* When looking at the same file in both windows (splitscreen), only the
  current window would be updated when inserting, cutting or copying.

* Pressing e.g CTRL+U in textfield no longer prints a ''.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.90á - 02 sep 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ Insert now toggles between insert and overwrite mode. Previously it
  just inserted a byte at the current position. To insert a byte now,
  press ALT+I.

+ Aaah, yes! Finally there is a clipboard with cut, copy and paste
  functions!

+ If you try to quit and have made changes to a file, HexIt now asks you
  whether you want to quit, save & quit, or cancel.

+ Now the statusrow(s) really displays some status! Read HEXIT.DOC for
  more info on _what_ they display.

* It's now possible to run HexIt from an OS/2-shell, previously it could
  only be run from a dos-shell under OS/2 (or of course from pure
  MS-DOS).

* Improved non-epileptic function... =) What I mean is that in the
  previous versions av HexIt, there was a lot of flicker on the screen
  when switching active file, or switching window for example. This is
  now removed in many places, thus causing a nicer environment.

* If you had the same file in both two windows previously, and deleted
  enough bytes in one window, to cause the other windows filebufferptr
  to get out of range, then when returning to the other window, you
  would find yourself running around in silicon heaven...

* Previosly when running e.g "HEXIT PKZ-STAT.EXE", HexIt would warp into
  setupmode... Not any more!	       ^^

* Fixed a bug that would have caused the system to crash if I had done
  it in another way earlier... :-)

* There was an error in my END-key routine that caused strange behaviour
  with some files. (Thanks PKaze!)

* The system would previously probably have crashed if trying to insert
  a byte when there was no memory left.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.84á - 27 aug 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
* Upgraded from PMODE 2.40 to PMODE 2.50. Some bug in the previous
  version caused HexIt not to work under OS/2 (maybe under any
  DPMI-server, I can't tell, since I usually dont work under DPMI).

* When you wrote something at the last byte, your position in the file
  was wrongly updated, causing you to start writing at the file
  immidiately following the active one. This is fixed.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.83á - 16 aug 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ Backspace works allright now.

+ Mmmm, it is now possible to delete bytes using DELete, the rest of the
  file will then be moved back one step to fill in the deleted byte.

+ Yupp, now you can insert bytes anywhere in the file! And what key do
  you think you use for that? Yes, it's INSert.

* Fixed a bug that caused the last row to get messy with files evenly
  divisible by 16. (Thanks Hannes!)

* When trying to move downwards in files shorter than 17 bytes, it
  simply was possible to move beyond the file. Not any more.

* Well, all you limit-freaks, be happy, 'cause you can now have 50 files
  in memory at the same time! That should be enough for everyone! Yupp,
  I know, Bill said something similar a couple of years ago, but... =8)


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.82á - 12 aug 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ A simple setupprogram, enabling you to customize HexIt's colors.

+ You can now edit and save files. Wow! =:)

+ There is now a big flashing cursor at the active pos.


			 ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
			 ³v0.81á - 10 aug 1995³
			 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
+ Yipppii, the first public version of HexIt opens it's foggy eyes,
  imbibes the knowledge of it's predecessors and starts evolving.

