# Lab Report 3 By Kevin Nie

## Grep Command

For this lab report, I have chosen the `grep` command. The `grep` command is a powerful tool for searching and filtering text. It is used to search text and strings in a given file. It allows you to find specific patterns in text files and display the lines containing those patterns. I have found four interesting command-line options for `grep` and provided two examples for each option using files and directories from `./technical`.

### 1. -i (ignore case)

The `-i` option allows you to perform a case-insensitive search. This is helpful when you want to find a pattern regardless of the text's capitalization. I searched the information from https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/.

**Example 1:**

```
$ grep -i 'Third' ./technical/911report/chapter-1.txt
    At 8:34, the Boston Center controller received a third transmission from American 11:
    FAA: Yes. This could be a third aircraft.
    The mention of a "third aircraft" was not a reference to American 77. There was confusion at that moment in the FAA. Two planes had struck the World Trade Center, and Boston Center had heard from FAA headquarters in Washington that American 11 was still airborne. We have been unable to identify the source of this mistaken FAA information.
    The Langley fighters were heading east, not north, for three reasons. First, unlike a normal scramble order, this order did not include a distance to the target or the target's location. Second, a "generic" flight plan-prepared to get the aircraft airborne and out of local airspace quickly-incorrectly led the Langley fighters to believe they were ordered to fly due east (090) for 60 miles. Third, the lead pilot and local FAA controller incorrectly assumed the flight plan instruction to go "090 for 60" superseded the original scramble order.
    At 9:32, a third radio transmission came over the frequency:"Keep remaining sitting. We have a bomb on board." The controller understood, but chose to respond: "Calling Cleveland Center, you're unreadable. Say again, slowly." He notified his supervisor, who passed the notice up the chain of command. By 9:34, word of the hijacking had reached FAA headquarters.
    The defense of U.S. airspace on 9/11 was not conducted in accord with preexisting training and protocols. It was improvised by civilians who had never handled a hijacked aircraft that attempted to disappear, and by a military unprepared for the transformation of commercial aircraft into weapons of mass destruction. As it turned out, the NEADS air defenders had nine minutes' notice on the first hijacked plane, no advance notice on the second, no advance notice on the third, and no advance notice on the fourth.
    Third, NEADS needed orders to pass to the pilots. At 10:10, the pilots over Washington were emphatically told, "negative clearance to shoot." Shootdown authority was first communicated to NEADS at 10:31. It is possible that NORAD commanders would have ordered a shootdown in the absence of the authorization communicated by the Vice President, but given the gravity of the decision to shoot down a commercial airliner, and NORAD's caution that a mistake not be made, we view this possibility as unlikely.
```
This command searches for the word 'Third' in the chapter-1.txt file, ignoring the case. It returns all the lines with the keyword, including "third" and "Third". The keyword is highlighted in the terminal. Useful for finding all related information regardless of case.

**Example 2:**

```
$ grep -i 'method' ./technical/biomed/1468-6708-3-1.txt
        Materials and methods
          years, using validated methods presented elsewhere [ 20 ]
```
This command searches for the word 'method' in the 1468-6708-3-1.txt file, ignoring the case. It returns all the lines with the keyword "method", and the keyword is highlighted in the terminal. Useful to check the method, regardless of case.


### 2. -r (recursive)
The `-r` option allows you to search for a pattern recursively through directories and their subdirectories. This command look for all files in the current directory and in all of its subdirectories. I searched the information from https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/ and ChatGPT.

**Example 1:**

```
$ grep -r 'maximum value' ./technical
./technical/biomed/1471-2164-4-28.txt:        to detect large ratios. For instance, the maximum value of
./technical/biomed/1471-2253-2-4.txt:        %maxTOTPAR by division into the calculated maximum value [
./technical/biomed/1471-2288-3-8.txt:          reaches the maximum value of ± ψ 
./technical/biomed/1471-2288-3-8.txt:           denote the anticipated maximum value of ψ 
./technical/biomed/1475-925X-2-6.txt:          (22)-(24) and (28)-(30) achieve their maximum values near
./technical/biomed/cc1476.txt:        tidal expiratory flow to a maximum value in adult patients
./technical/biomed/gb-2002-3-7-research0036.txt:             is the maximum value of the statistic 
./technical/biomed/gb-2002-3-7-research0036.txt:          much weaker. In particular, for Clest, the maximum value
./technical/plos/journal.pbio.0020354.txt:        barcoding could have maximum value. In general, among-population sequence divergence
./technical/plos/pmed.0020059.txt:          gradually increase the circle radius from zero to some maximum value defined by the user,
```
This command searches for the keyword 'maximum value' recursively in all files and directories within technical. Useful for finding out some patterns about maximum values and which files to look at.

**Example 2:**

```
$ grep -r 'Chinese' ./technical/911report
./technical/911report/chapter-11.txt:                surprise attacks before-Pearl Harbor is one well-known case, the 1950 Chinese attack
./technical/911report/chapter-13.3.txt:                of the CIA over the recent bombing of the Chinese embassy in Belgrade was at its
./technical/911report/chapter-3.txt:                just led the United States to mistakenly bomb the Chinese embassy in Belgrade during
./technical/911report/chapter-6.txt:                over a U.S." spy plane" brought down in Chinese territory. The new administration
```
This command searches for the word 'Chinese' recursively in all files and directories within 911report. Useful to see how Chinese are involved in the reports and get their file names for further references.


### 3. -n (line number)
The `-n` option displays the line number along with the output. This is useful for finding the exact location of a pattern within a file. I searched the information from `man grep` and ChatGPT.

**Example 1:**

```
$ grep -n 'sitting' ./technical/911report/chapter-1.txt
52:    At 7:50, Majed Moqed and Khalid al Mihdhar boarded the flight and were seated in 12A and 12B in coach. Hani Hanjour, assigned to seat 1B (first class), soon followed. The Hazmi brothers, sitting in 5E and 5F, joined Hanjour in the first-class cabin.
70:    At the same time or shortly thereafter, Atta-the only terrorist on board trained to fly a jet-would have moved to the cockpit from his business-class seat, possibly accompanied by Omari. As this was happening, passenger Daniel Lewin, who was seated in the row just behind Atta and Omari, was stabbed by one of the hijackers-probably Satam al Suqami, who was seated directly behind Lewin. Lewin had served four years as an officer in the Israeli military. He may have made an attempt to stop the hijackers in front of him, not realizing that another was sitting behind him.
176:    At 9:32, a hijacker, probably Jarrah, made or attempted to make the following announcement to the passengers of Flight 93:"Ladies and Gentlemen: Here the captain, please sit down keep remaining sitting. We have a bomb on board. So, sit." The flight data recorder (also recovered) indicates that Jarrah then instructed the plane's autopilot to turn the aircraft around and head east.
460:    At 9:32, a third radio transmission came over the frequency:"Keep remaining sitting. We have a bomb on board." The controller understood, but chose to respond: "Calling Cleveland Center, you're unreadable. Say again, slowly." He notified his supervisor, who passed the notice up the chain of command. By 9:34, word of the hijacking had reached FAA headquarters.
```
This command searches for the word 'sitting' in the `chapter-1.txt` file and displays the line number where the pattern is found. Useful for checking other lines if needed.

**Example 2:**

```
$ grep -n 'countries' ./technical/plos/journal.pbio.0020001.txt
7:        the clear inequalities in science between developing and developed countries and to the
11:        countries, asserting that “This unbalanced distribution of scientific activity generates
12:        serious problems not only for the scientific community in the developing countries, but for
15:        output between the developing and already developed countries (Gibbs 1995; May 1997;
18:        developed countries accounted for some 84% of the global investment in scientific research
29:        It is rather obvious that richer countries are able to invest more resources in science
37:        developing countries. For example, Latin America and China, although representing,
84:        Among Latin American countries, there is a high degree of variability in publication
85:        rate as well as in financial investment in science and technology. Some countries have
89:        United States (1.5) and even Canada (3.3) (RICYT 2002). Other countries, such as Costa
91:        research and development than the other countries of this region (Albornoz 2001).
103:        is that scientific development during the 1990s was particularly strong for many countries
139:        the top 11–20 (impact factors 3.28–2.47), the Latin American countries contributed nearly
218:        developing countries contribute a more equitable share to the international scientific
221:        development, demonstrates that many developing countries are heading in the right
```
This command searches for the word 'countries' in the `journal.pbio.0020001.txt` file and displays the line number where the pattern is found. Useful to see how different countries involved and which lines they are at for further reference.


### 4. -v (invert match)
The `-v` option inverts the match, meaning it shows the lines that do not contain the specified pattern. This is useful for filtering out unwanted information. I searched the information from `man grep` and ChatGPT.

**Example 1:**

```
$ grep -v 'e' ./technical/plos/journal.pbio.0020001.txt

  
    
      
        
        
          
          
        
      
      
        2002).
        
          
            Canada?
          
        
      
      
        programs.
      
      
        journals (
        In 
      
      
        world.
        
          
          
        
        built.
      
    
```
  This command filters out the lines containing the word 'e' from the `journal.pbio.0020001.txt` file and displays the remaining lines. It could be used to see how the vowel "e" is important in English.
  
**Example 2:**

```
$ grep -v 'animal' ./technical/plos/pmed.0020258.txt

  
    
      
        
        Animal models can play an essential role in guiding preclinical vaccine development,
        including in studies of preclinical vaccine safety, vaccine toxicity, and vaccine
        immunogenicity. Appropriate pathogen challenge models can also provide the opportunity to
        perform preclinical tests of vaccine efficacy. Preclinical tests of HIV vaccine efficacy
        are usually performed by exposing macaques to simian immunodeficiency virus (SIV), a virus
        that is closely related to HIV. However, the viral inoculum sizes used to infect macaques
        with SIV vastly exceed the amounts of HIV that humans are exposed to during a given
        preclinical tests of vaccine efficacy. Indeed, no vaccine has been shown to be effective in
        preventing infection by SIV (so-called sterilizing immunity) in such high viral inoculum
        trials. Now, in a paper published in 
        PLoS Medicine , Roland Regoes and colleagues speculate that an
        What the researchers did was use statistical power analysis to compare a single low-dose
        predetermined maximum number of challenges is reached. The statistical power of an
        experimental design—a measure of the statistical quality—was assessed by simulating
        experiments, evaluating them, and then repeating the procedure thousands of times.
        What they found was that the experimental design using a single low dose of virus in
        per group to reach a statistical power of 95%. However, when the researchers modeled a
        ID
        50 , and allowing for a maximum number of 20 challenges of each
        statistical power.
        Where do these results leave the design of HIV trials? To begin with, the results should
        possible, what is known about the natural history and pathogenesis of the disease in
        authors have made available the programming script of their analysis so anyone can repeat
        it; it would be interesting to know whether preclinical trials assessing vaccines or
        treatments against infections by other pathogens could be usefully modeled in this way as
        well.
      
    
```
This command filters out the lines containing the word 'animal' from the `pmed.0020258.txt` file and displays the remaining lines. It could be used to find lines unrelated to animals.

These examples demonstrate how the `grep` command can be a powerful tool for searching and filtering text. By using different command-line options, you can customize your search to be case-insensitive, recursive, display line numbers, or even invert the match. These could be helpful in further and more advanced searching.
