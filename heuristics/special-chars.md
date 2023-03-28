> This page has special characters in it. Where noted, copy and paste everything after the : 

#### Testing with ASCII Special Characters in UI

Actions:
  Create a new Object Cataloging record
  Add any number in Identification Number field

1. Variation A: In one single and one multiline text area, copy and paste: `"This sentence is wrapped in double quotes."`
2. Variation B: In one single and one multiline text area, copy and paste: `'single quotes'`
3. Variation C: In one single and one multiline text area, copy and paste: `[square brackets]`
4. Variation D: In one single and one multiline text area, copy and paste: `{curly braces}` 
5. Variation E: In one single and one multiline text area, copy and paste: `<angle brackets>`
6. Variation F: In one single and one multiline text area, copy and paste: `<! -- XML comment -->`
7. Variation H: In one single and one multiline text area, copy and paste: `"quoted" segment & ampersand`
8. Variation I: In one single and one multiline text area, copy and paste: `"A "quoted" segment; & (entity); wrapped in quotes"`
9. Variation K: In one single and one multiline text area, copy and paste: `back-quote: Hawai i`
10. Variation L: In one single and one multiline text area, copy and paste: `hash: #20`
11. Variation M: In one single and one multiline text area, copy and paste: `escaped slash: \/`
12. Save the record

Expected:
After the successful save message appears, all fields should contain the same value as you entered

#### Testing with Non-ASCII Characters in UI

Actions:
  Continue from previous (or open an existing Object cataloging record)

 1. In one single and one multiline text area, copy and paste: café
 2. Be sure characters paste as shown
 3. In one single and one multiline text area, copy and paste:
    > `ñóǹ äŝçíì 汉语/漢語  华语/華語 Huáyǔ; 中文 Zhōngwén 漢字仮名交じり文 Lech Wałęsa æøå`
 4. Save the record

Expected:
After the successful save message appears, all fields should contain the same value as you entered

#### Testing with Strings of over 500 characters

Actions:
  Continue from Test 1 (or open an existing Object cataloging record)

In at least one text area (multiline text field), paste or enter text containing more than 500 characters. 
  Example:
   > START 
   > 
   > 1) I am typing in more than 500 characters of text to test whether the more than 500 characters are cut off or if they display correctly. 500
   > characters is a lot of text. 
   > 2) I am typing in more than 500 characters of text to test whether the more than 500 characters are cut off or if they display correctly. 500
   > characters is a lot of text. 
   > 3) I am typing in more than 500 characters of text to test whether the more than 500 characters are cut off or if they display correctly. 500
   > characters is a lot of text. 
   > 
   > END

Save the record

Expected:
After the successful save message appears, text area should contain the same characters as you entered and should not be cut off

#### Testing Activity! 🦄  Spend 3 minutes trying to break something!

Spend a few minutes forcing the program to expose buggy behavior by:
- Use the system in ways not covered by the testplan
- Use the system in unexpected ways
- Do whatever you can think of that will produce bugs and unexpected behavior
- Be creative!
- Feel free to extend this to behavior related to your testplan
