# Lab Report 3 By Kevin Nie

## Grep Command

For this lab report, I have chosen the `grep` command. The `grep` command is a powerful tool for searching and filtering text. It is used to search text and strings in a given file. It allows you to find specific patterns in text files and display the lines containing those patterns. I have found four interesting command-line options for `grep` and provided two examples for each option using files and directories from `./technical`.

### 1. -i (ignore case)

The `-i` option allows you to perform a case-insensitive search. This is helpful when you want to find a pattern regardless of the text's capitalization. I searched the information from https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/.

**Example 1:**

```
$ grep -i 'sitting' ./technical/911report/chapter-1.txt
    At 7:50, Majed Moqed and Khalid al Mihdhar boarded the flight and were seated in 12A and 12B in coach. Hani Hanjour, assigned to seat 1B (first class), soon followed. The Hazmi brothers, sitting in 5E and 5F, joined Hanjour in the first-class cabin.
    At the same time or shortly thereafter, Atta-the only terrorist on board trained to fly a jet-would have moved to the cockpit from his business-class seat, possibly accompanied by Omari. As this was happening, passenger Daniel Lewin, who was seated in the row just behind Atta and Omari, was stabbed by one of the hijackers-probably Satam al Suqami, who was seated directly behind Lewin. Lewin had served four years as an officer in the Israeli military. He may have made an attempt to stop the hijackers in front of him, not realizing that another was sitting behind him.
    At 9:32, a hijacker, probably Jarrah, made or attempted to make the following announcement to the passengers of Flight 93:"Ladies and Gentlemen: Here the captain, please sit down keep remaining sitting. We have a bomb on board. So, sit." The flight data recorder (also recovered) indicates that Jarrah then instructed the plane's autopilot to turn the aircraft around and head east.
    At 9:32, a third radio transmission came over the frequency:"Keep remaining sitting. We have a bomb on board." The controller understood, but chose to respond: "Calling Cleveland Center, you're unreadable. Say again, slowly." He notified his supervisor, who passed the notice up the chain of command. By 9:34, word of the hijacking had reached FAA headquarters.
```
This command searches for the word 'sitting' in the chapter-1.txt file, ignoring the case. It returns all the lines with the keyword "sitting", and the keyword is highlighted in the terminal.
