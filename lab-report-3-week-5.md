# Lab Report 3

## `Grep` Command Options

### `grep -i`

```
[cs15lfa22fw@ieng6-201]:docsearch:339$ grep -i "bye" technical/*/*.txt
technical/911report/chapter-1.txt:    At 9:57, the passenger assault began. Several passengers had terminated phone calls with loved ones in order to join the revolt. One of the callers ended her message as follows:"Everyone's running up to first class. I've got to go. Bye."
technical/911report/chapter-7.txt:                families to say goodbye, something he had forbidden. Atta, moreover, was nervous
technical/911report/chapter-7.txt:                Binalshibh to contact the family of one hijacker, pass along goodbyes from others,
technical/biomed/1477-7819-1-10.txt:        clinically negative. On the contrary Byers et al (1997) [ 3
technical/plos/journal.pbio.0020419.txt:        weeks.) Was it his way of saying goodbye, of bringing his extended family close again? We
```

**BLOCK 1 - This block is searching within directory technical and within every subdirectories for files that contain the word "bye" in them and display their paths.**

```
[cs15lfa22fw@ieng6-201]:docsearch:340$ grep -i "ByE" technical/911report/*.txt
technical/911report/chapter-1.txt:    At 9:57, the passenger assault began. Several passengers had terminated phone calls with loved ones in order to join the revolt. One of the callers ended her message as follows:"Everyone's running up to first class. I've got to go. Bye."
technical/911report/chapter-7.txt:                families to say goodbye, something he had forbidden. Atta, moreover, was nervous
technical/911report/chapter-7.txt:                Binalshibh to contact the family of one hijacker, pass along goodbyes from others,
```

**BLOCK 2 - This block is searching within the technical directory and within the 911report subdirectory for a .txt file that contains the word "bye" ignores its capitalization.**

```
[cs15lfa22fw@ieng6-201]:docsearch:341$ grep -i "ToDAY" technical/911report/*.txt
technical/911report/chapter-10.txt:                assign tasks for the first wave of the war against terrorism. It starts today."
technical/911report/chapter-11.txt:                risks. Given how hard it has proved to locate Bin Ladin even today when there are
technical/911report/chapter-12.txt:                the front lines fighting terrorists today, we asked them: If you were a terrorist
technical/911report/chapter-12.txt:                leader today, where would you locate your base? Some of the same places come up
technical/911report/chapter-12.txt:            We offer three illustrations that are particularly applicable today, in 2004:
technical/911report/chapter-12.txt:                10,000 American soldiers are deployed today in Afghanistan, joined by soldiers from
technical/911report/chapter-12.txt:                figures find it difficult to publicly defend good relations with the other. Today,
technical/911report/chapter-12.txt:                    today, a terrorist can defeat the link to electronic records by tossing away an
technical/911report/chapter-12.txt:                coming into the country. Today more than 9 million people are in the United States
technical/911report/chapter-13.1.txt:                confronts a very different world today. Instead of facing a few very dangerous
technical/911report/chapter-13.1.txt:                Today the CIA is still central. But the FBI is much more active, along with
technical/911report/chapter-13.1.txt:                some of their turf and authorities and prerogatives." Today, he said, the executive
technical/911report/chapter-13.1.txt:                today. Opponents of declassification argue that America's enemies could learn about
technical/911report/chapter-13.3.txt:                Call for Safety Measures: The FAA Is Expected to Release a Report Today," Fort Worth
technical/911report/chapter-13.3.txt:                June 26, 2002. Today, Sudan is still listed as a state sponsor of terrorism.
technical/911report/chapter-13.5.txt:                Cauchon and Martha Moore,"Miracles Emerge from Debris," USA Today, Sept. 6, 2002, p.
technical/911report/chapter-13.5.txt:                16, 2003, then Malaysian prime minister Mahathir Mohamad said:"Today we, the whole
technical/911report/chapter-13.5.txt:                enemies, which he argued were controlled by the Jews. "But today the Jews rule the
technical/911report/chapter-13.5.txt:                www.usatoday.com/news/washington/executive/rumsfeld-memo.htm).
technical/911report/chapter-2.txt:                in the world today and the worst terrorists are the Americans. Nothing could stop
technical/911report/chapter-2.txt:                more tranquil world, he offers his "Caliphate" as an imagined alternative to today's
technical/911report/chapter-2.txt:                Arab Middle East followed an arc from initial pride and optimism to today's mix of
technical/911report/chapter-2.txt:                countries such as Saudi Arabia, Morocco, and Jordan still survive today. Those in
technical/911report/chapter-2.txt:                victory, triggering a brutal civil war that continues today. Opponents of today's
technical/911report/chapter-3.txt:                Intelligence of the Coast Guard; and, today, the Directorate of Intelligence
technical/911report/chapter-3.txt:                build technical systems to break ciphers and to make sense of today's complex
technical/911report/chapter-3.txt:            An innovation of Donovan's, whose legacy remains part of U.S. intelligence today, was
technical/911report/chapter-3.txt:                During the 1990s and today, particular value is attached to having a contribution
technical/911report/chapter-3.txt:                modern Armed Services committees that have become so powerful today. One especially
technical/911report/chapter-3.txt:                unit chief, "Mike," agreed. Schroen believes today that this was a lost opportunity
technical/911report/chapter-3.txt:                the time and today, it was hard for them to imagine how any intelligence on Bin
technical/911report/chapter-8.txt:            Although we readily equate KSM with al Qaeda today, this was not the case before
technical/911report/chapter-9.txt:            The first responders of today live in a world transformed by the attacks on 9/11.
```

**BLOCK 3 - This block shows that the computer is searching for every .txt files in the 911report subdirectory that contains the word "Today" ignores captitalization.**

*The purpose of `Grep -i` is to search for a line inside of every files that match the given string ignores capitalization. We can use this command to find which file has the string including both upper case and lower case.*

### `grep -n`

```
[cs15lfa22fw@ieng6-201]:docsearch:342$ grep -n "bye" technical/911report/*.txt
technical/911report/chapter-7.txt:1217:                families to say goodbye, something he had forbidden. Atta, moreover, was nervous
technical/911report/chapter-7.txt:1407:                Binalshibh to contact the family of one hijacker, pass along goodbyes from others,
```

**BLOCK 1 - This block is searching for the .txt files within the 911report subdirectory that contains the word "bye" and also prints the line number that the word is in.**

```
[cs15lfa22fw@ieng6-201]:docsearch:345$ grep -n -i "bye" technical/*/*.txt        
technical/911report/chapter-1.txt:198:    At 9:57, the passenger assault began. Several passengers had terminated phone calls with loved ones in order to join the revolt. One of the callers ended her message as follows:"Everyone's running up to first class. I've got to go. Bye."
technical/911report/chapter-7.txt:1217:                families to say goodbye, something he had forbidden. Atta, moreover, was nervous
technical/911report/chapter-7.txt:1407:                Binalshibh to contact the family of one hijacker, pass along goodbyes from others,
technical/biomed/1477-7819-1-10.txt:151:        clinically negative. On the contrary Byers et al (1997) [ 3
technical/plos/journal.pbio.0020419.txt:170:        weeks.) Was it his way of saying goodbye, of bringing his extended family close again? We
```

**BLOCK 2 - This block is searching for the .txt files within every subdirectories that contains the word "bye" ignores capitalization and also prints the line number that the word is in.**

```
[cs15lfa22fw@ieng6-201]:docsearch:347$ grep -n "Today" technical/911report/*.txt
technical/911report/chapter-12.txt:487:                figures find it difficult to publicly defend good relations with the other. Today,
technical/911report/chapter-12.txt:1191:                coming into the country. Today more than 9 million people are in the United States
technical/911report/chapter-13.1.txt:68:                Today the CIA is still central. But the FBI is much more active, along with
technical/911report/chapter-13.1.txt:159:                some of their turf and authorities and prerogatives." Today, he said, the executive
technical/911report/chapter-13.3.txt:850:                Call for Safety Measures: The FAA Is Expected to Release a Report Today," Fort Worth
technical/911report/chapter-13.3.txt:1133:                June 26, 2002. Today, Sudan is still listed as a state sponsor of terrorism.
technical/911report/chapter-13.5.txt:2071:                Cauchon and Martha Moore,"Miracles Emerge from Debris," USA Today, Sept. 6, 2002, p.
technical/911report/chapter-13.5.txt:2856:                16, 2003, then Malaysian prime minister Mahathir Mohamad said:"Today we, the whole
```

**BLOCK 3 - This block is searching for the .txt files within the 911report subdirectory that contains the word "Today" and also prints the line number that the word is in.**

*The purpose of `grep -n` is to search for a line within the file within some directory that contains certain words and print the line number within that file as well. We can use this to look for the line number that contains the "word" in our program.*

## `grep -A or grep -B or grep -C`

```
[cs15lfa22fw@ieng6-201]:docsearch:348$ grep -A4 "bye" technical/911report/chapter-7.txt 
                families to say goodbye, something he had forbidden. Atta, moreover, was nervous
                about his future communications with Binalshibh, whom he instructed to obtain new
                telephones upon returning to Germany. Before Binalshibh left Spain, he gave Atta
                eight necklaces and eight bracelets that Atta had asked him to buy when he was
                recently in Bangkok, believing that if the hijackers were clean shaven and well
--
                Binalshibh to contact the family of one hijacker, pass along goodbyes from others,
                and give regards to KSM. Jarrah alone appears to have left a written farewell-a
                sentimental letter to Aysel Senguen.

            Hazmi, however, may not have been so discreet. He may have telephoned his former San
```

**BLOCK 1 - This block is searching within the chapter-7.txt file within the 911report subdirectory whether it has the word "bye" or not. If it does print the line that contains the word "bye" and 4 line after it as well.**

```
[cs15lfa22fw@ieng6-201]:docsearch:350$ grep -B2 "bye" technical/*/*
technical/911report/chapter-7.txt-                and each team would be able to command the passengers in English. According to
technical/911report/chapter-7.txt-                Binalshibh, Atta complained that some of the hijackers wanted to contact their
technical/911report/chapter-7.txt:                families to say goodbye, something he had forbidden. Atta, moreover, was nervous
--
technical/911report/chapter-7.txt-                messaging. Although Atta had forbidden the hijackers to contact their families, he
technical/911report/chapter-7.txt-                apparently placed one last call to his own father on September 9. Atta also asked
technical/911report/chapter-7.txt:                Binalshibh to contact the family of one hijacker, pass along goodbyes from others,
grep: technical/government/About_LSC: Is a directory
grep: technical/government/Alcohol_Problems: Is a directory
grep: technical/government/Env_Prot_Agen: Is a directory
grep: technical/government/Gen_Account_Office: Is a directory
grep: technical/government/Media: Is a directory
grep: technical/government/Post_Rate_Comm: Is a directory
--
technical/plos/journal.pbio.0020419.txt-        working lunches at home with Odile, his wife of fifty-five years. Why do this? Why all this
technical/plos/journal.pbio.0020419.txt-        focus on another part of the brain, when only months remained? (Indeed it turned out to be
technical/plos/journal.pbio.0020419.txt:        weeks.) Was it his way of saying goodbye, of bringing his extended family close again? We
```

**BLOCK 2 - This block is searching within every files within every subdirectory inside of the technical directory that contains the word "bye". Then print out all the line that contains the word "bye" and 2 line after it as well. However, within the government subdirectory, there isn't any file, but rather some more subdirectories, so it grep gives some errors.**

```
[cs15lfa22fw@ieng6-201]:docsearch:357$ grep -C1 -i "nice" technical/911report/*
technical/911report/chapter-7.txt-            We do not pick up their trail until February 1, 2000, when they encountered Omar al
technical/911report/chapter-7.txt:                Bayoumi and Caysan Bin Don at a halal food restaurant on Venice Boulevard in Culver
technical/911report/chapter-7.txt-                City, a few blocks away from the King Fahd mosque. Bayoumi and Bin Don have both
--
technical/911report/chapter-7.txt-                contrast, Ziad Jarrah had already arranged to attend the Florida Flight Training
technical/911report/chapter-7.txt:                Center (FFTC) in Venice, Florida. Jarrah arrived in Newark on June 27 and then flew
technical/911report/chapter-7.txt:                to Venice. He immediately began the private pilot program at FFTC, intending to get
technical/911report/chapter-7.txt-                a multi-engine license. Jarrah moved in with some of the flight instructors
--
technical/911report/chapter-7.txt-                Qaeda operative, Ihab Ali, had taken lessons in the mid1990s), Atta started flight
technical/911report/chapter-7.txt:                instruction at Huffman Aviation in Venice, Florida, and both Atta and Shehhi
technical/911report/chapter-7.txt-                subsequently enrolled in the Accelerated Pilot Program at that school. By the end of
--
technical/911report/chapter-7.txt-                2001. In late September, they decided to enroll at Jones Aviation in Sarasota,
technical/911report/chapter-7.txt:                Florida, about 20 miles north of Venice. According to the instructor at Jones, the
technical/911report/chapter-7.txt-                two were aggressive, rude, and sometimes even fought with him to take over the
```

**BLOCK 3 - This block is searching within every files inside of the 911report subdirectory that contains the word "nice" ignores capitalization. Then print out all the line that contains the word "nice" and 1 line after it as well.**

*The purpose of `grep -A or grep -B or grep -C` is to search for the file that contains the "word" and print the search line and n number of lines after the search line. We can use this command to look for the error line in our code and also look at the lines of code after it as well.*