# Bandit Wargame Notes

## Level 0 → 1
Easy server connection, usually goes like `USERNAME@website-link` along with the side port number (the gate they want you to connect to).

---

## Level 1 → 2
Had to use the technique called `./-` for the `-` folder so it doesn't get flagged.

---

## Level 2 → 3
The password was in a file with spaces: `"spaces in this filename"` — literally had to use `cat --` to indicate that everything after it is a file, telling the system not to flag it.

---

## Level 3 → 4
It was a hidden file inside the `inhere` folder. Had to use `ls -alps` to reveal everything.

---

## Level 4 → 5
Just had to `cd` into folders until you found the human-readable files.

---

## Level 5 → 6
Had to use the `find` command with the following parameters:
- `-type f` — files only
- `-size 1033c` — specific size
- `!-executable` — not executable

---

## Level 6 → 7
Had to use `find` again but with `/` to search the whole server. Added parameters:
- `-user` — the owner
- `-group` — the way to give a bunch of users permission

---

## Level 7 → 8
Using `grep "<word you want>"` prints the whole line that contains that word.

---

## Level 8 → 9
Using `sort data.txt | uniq -u` (unique thing that appears only once). The `|` pipe uses the output from the left command as input for the right — shows you the answer.

---

## Level 9 → 10
Use `strings` to show human-readable content, then pipe into `grep` to finish the job.

---

## Level 10 → 11
Had to use `base64` to decode the answer.

---

## Level 11 → 12
Using `tr` (translate/transliterate) — acts like a substitution tool. The challenge asked you to decode using **ROT13**, which replaces each letter with the one 13 positions ahead in the alphabet (e.g. A → N). The command uses `<` for input redirection.

---

## level 12 -> 13
For this one, it was a lot of going back and forth because of the thing being that it was compressed through so much use of Gzip, Bzip2, and even Tar utility archive. Crazy Work, you have to use command like <tar -xf> (-x (extract) the -f (files)), <gzip -d (decompress)> and <bzip2 -d> also does the same thing as gzip basically

---
## level 13 -> 14
