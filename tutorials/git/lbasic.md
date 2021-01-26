---
description: >-
  Some of the most common Linux commands and their usages listed in the table
  below. Commands are sorted based on popularity whereas shortcuts are sorted
  alphabetically.
---

# Linux \| Shell Basics

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Command Type</b>
      </th>
      <th style="text-align:left"><b>Usage</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Intro - Basic Symbols</b>
      </td>
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(Slash) /</code></b>
      </td>
      <td style="text-align:left">
        <p>Used to denote following directories in the root tree</p>
        <ul>
          <li><code>/parent/child</code>directs to <b>child</b> folder inside the <b>parent</b> folder</li>
          <li><code>/parent/child/file1.txt</code> directs to <b>file1</b> text file inside
            the <b>child</b> folder, etc.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(Tilde) ~</code></b>
      </td>
      <td style="text-align:left">
        <p>Shortcut for the home directory - <code>/home/username</code>
        </p>
        <ul>
          <li><code>~/Desktop</code> means <code>/home/username/Desktop</code>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(Dot) .</code></b>
      </td>
      <td style="text-align:left">
        <p>Stands for the current directory you are located in</p>
        <ul>
          <li>Say you are in <code>dir1/dir2/dir3</code> directory
            <ul>
              <li><b><code>.</code></b> represents <code>dir1/dir2/dir3</code>(current dir)</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(2 Dots) ..</code></b>
      </td>
      <td style="text-align:left">
        <p>Stands for the parent directory (one directory up in the tree)</p>
        <ul>
          <li><code>..</code> represents <code>dir1/dir2</code> directory (1 dir up)</li>
          <li><code>../..</code> represents <code>/dir1 </code> directory (2 dir up)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(Dash) -</code></b>
      </td>
      <td style="text-align:left">
        <p>Stands for the recent directory located (or flags see below)</p>
        <ul>
          <li><b><code>-</code></b> represents<code>dir1/dir2</code> (previous directory)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(Backward Slash) \</code></b>
      </td>
      <td style="text-align:left">
        <p>Used to skip characters if the name includes a space</p>
        <ul>
          <li>Either use <code>\</code> or put inside a string to denote a new including
            a blank in the path name</li>
          <li><code>/dir1/new\ file</code> or <code>&quot;/dir1/new file.txt&quot;</code>is
            used to denote the <b>&quot;new file.txt&quot; </b>text file in the <b>dir1</b> folder</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(Asterisk) *</code></b>
      </td>
      <td style="text-align:left">
        <p>Used as a <em>wildcard</em> during searches - matches one of more occurrences
          of any character, including no character</p>
        <ul>
          <li><code>ls -l a*</code> lists all files whose name is starting with <b>a</b>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(Question Mark) ?</code></b>
      </td>
      <td style="text-align:left">
        <p>Used as a <em>wildcard</em> to represent an anonymous character</p>
        <ul>
          <li><code>ls e?d</code>lists all 3-character files starts with <b>e</b> and <b>d</b>
            <ul>
              <li>Possible results <b>end, eid</b>, etc.</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>(Brackets) [chars]</code></b>
      </td>
      <td style="text-align:left">
        <p>Used as a <em>wildcard</em> to represent a character between brackets</p>
        <ul>
          <li><code>ls l[aeoi]st</code>lists all 4-character files starts with <b>l</b> ands
            with <b>st</b> if <b>[aeoi]</b> is one of the middle character.
            <ul>
              <li>Possible results <b>last, lost, list</b>, etc.</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>&lt;command&gt; -options</code></b>
      </td>
      <td style="text-align:left">
        <p>Characters after a dash symbol following a command stands for options
          (flags) for that command to be executed</p>
        <ul>
          <li>Example: <code>ls</code> lists files in the current folder whereas <code>ls -a</code> lists
            all - including hidden ones</li>
          <li>Options (flags) for each command can be found in manual - use <code>man &lt;command&gt;</code> to
            see details</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>/home/username/.../file</code></b>
      </td>
      <td style="text-align:left"> <b>Absolute path</b> of a file from the <b>root</b> folder - <em>always works!</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>../dir1/dir2/file</code></b>
      </td>
      <td style="text-align:left">
        <p> <b>Relative path</b> to a <b>file</b> relative to the current directory</p>
        <ul>
          <li>Say you are in <code>~/Desktop/dir1/dir2/file.txt</code>
          </li>
          <li>Absolute path of <b>dir1</b> folder is:
            <ul>
              <li><code>/home/username/Desktop/parent</code>
              </li>
            </ul>
          </li>
          <li>Relative path of <b>dir1 </b>to <b>file.txt </b>file is:
            <ul>
              <li><code>..</code>(Notice we are still in <b>dir2 </b>folder)</li>
            </ul>
          </li>
        </ul>
        <p></p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Navigation Commands</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>pwd</code></b>
      </td>
      <td style="text-align:left">Prints working directory (absolute path)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cd &lt;dir&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Changes directory to dir (folder)</p>
        <ul>
          <li><code>cd .</code> moves to current dir (output of<code>pwd</code>)</li>
          <li><code>cd ..</code> moves 1 directory up</li>
          <li><code>cd ../..</code><b><code> </code></b>moves 2 directory up</li>
          <li><code>cd -</code><b><code>     </code></b>prints and moves to the recent
            directory</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>ls &lt;dir&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Lists all (excluding hidden) files in a given / current dir</p>
        <ul>
          <li>Use <code>-a</code> flag to list hidden files (<code>.hiddenfile</code>)</li>
          <li>Use <code>-l</code> to list files in the tabular (long) format</li>
          <li>Some flags can be combined - Example: <code>ls -al</code>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>man &lt;command&gt;</code></b>
      </td>
      <td style="text-align:left">Opens the user manual for the command</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>&lt;command&gt; --help</code></b>
      </td>
      <td style="text-align:left">Opens the help page for the command</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>time &lt;command&gt;</code></b>
      </td>
      <td style="text-align:left">Prints the time it takes to execute the command</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>history</code></b>
      </td>
      <td style="text-align:left">Prints the last commands typed on the terminal</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>clear</code></b>
      </td>
      <td style="text-align:left">Clears the terminal page (Ctrl+L)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cat</code></b>
      </td>
      <td style="text-align:left">Concatenate - Multiple purpose</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>file &lt;filename&gt;</code></b>
      </td>
      <td style="text-align:left">Displays the type of file given with <b>filename</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>locate &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">Locates (searches for) the file in the Linux system</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>shutdown &lt;time&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Shuts down the system at a given time</p>
        <ul>
          <li><code>shutdown -h now</code> - Shuts down the system immediately</li>
          <li><code>shutdown -r now</code> - Reboot the system immediately</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>reboot</code></b>
      </td>
      <td style="text-align:left">Stops and restarts the system</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>reset</code></b>
      </td>
      <td style="text-align:left">Resets the terminal screen</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>exit</code></b>
      </td>
      <td style="text-align:left">Logs out of terminal (Ctrl+D)</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Displaying System Info</b>
      </td>
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>w</code></b>
      </td>
      <td style="text-align:left">Displays the online user information</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>whoami</code></b>
      </td>
      <td style="text-align:left">Displays the current <b>username</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>date</code></b>
      </td>
      <td style="text-align:left">
        <p>Prints the full date with other details</p>
        <ul>
          <li>(Default): <code>Day Month #Day hh:mm:ss TimeZone yyyy</code>
          </li>
          <li>Example: <code>Mon Jan 25 14:18:52 CST 2021</code>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cal</code></b>
      </td>
      <td style="text-align:left">Displays the monthly calendar</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>finger &lt;user&gt;</code></b>
      </td>
      <td style="text-align:left">Displays user information</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>du</code></b>
      </td>
      <td style="text-align:left">Shows directory space usage</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>df</code></b>
      </td>
      <td style="text-align:left">Shows a report on the disk space usage</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>whereis &lt;app&gt;</code></b>
      </td>
      <td style="text-align:left">Displays the location of the application</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>which &lt;app&gt;</code></b>
      </td>
      <td style="text-align:left">Displays the default version of the app</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Displaying File Contents</b>
      </td>
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>echo &lt;&quot;string&quot;&gt;</code></b>
      </td>
      <td style="text-align:left">Prints the string</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cat &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">Prints the contents of the file</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>open &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">Opens the file in the given path</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>less &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Displays the contents of the file</p>
        <ul>
          <li>Can navigate forward and backward through file</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>more &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Displays the contents of the given file</p>
        <ul>
          <li>Allows users to scroll up &amp; down through pages</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>head # &lt;text&gt;</code></b>
      </td>
      <td style="text-align:left">Displays<b> the first </b><code>#</code> lines of the text file</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>tail # &lt;text&gt;</code></b>
      </td>
      <td style="text-align:left">Displays <b>the last</b>  <code>#</code> lines of the text file</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>grep &lt;content&gt; &lt;text&gt;</code></b>
      </td>
      <td style="text-align:left">Searches (filters) for the <b>content </b>in the text file</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>sort &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">Sorts the contents of the file</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>wc &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">Displays the number of words (word count) in the file</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>File Manipulation</b>
      </td>
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>mkdir &lt;name&gt;</code></b>
      </td>
      <td style="text-align:left">Makes directory with the given name</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>mv &lt;file&gt; &lt;dir&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Moves the given file to the given directory</p>
        <ul>
          <li>Can be used to rename files ass well
            <ul>
              <li><code>mv &lt;file_name&gt; &lt;new_name&gt;</code>
              </li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>rm &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Removes the given file - <b>cannot be undone</b>
        </p>
        <ul>
          <li>Can<b>not</b> remove directories unless used with <code>-r</code> option
            <ul>
              <li><code>rm -r &lt;dir&gt; </code>- <b>Recursively</b> deletes all files in
                dir</li>
              <li><code>rm -rf &lt;dir&gt;</code> - Does <b>not</b> ask for permit</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>rmdir &lt;dir&gt;</code></b>
      </td>
      <td style="text-align:left">Removes the given directory <b>if it is empty</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>touch &lt;file1&gt; &lt;file2&gt;</code></b>
      </td>
      <td style="text-align:left">Creates a new file or files - <em>file 1</em> (and <em>file 2</em>)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cp &lt;file&gt; &lt;new_name&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Copies the given file with a given new name</p>
        <ul>
          <li>Can copy directories <b>recursively</b> with <code>-r</code> option
            <ul>
              <li><code>cp -r &lt;dir&gt; &lt;new_name&gt;</code>
              </li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cut &lt;options&gt; &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">Cuts a specific part of the file</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>ln &lt;source&gt; &lt;link&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Creates a physical / symbolic (<code>-s</code> option) links between files
          <br
          />In order to remove the symbolic links use either:</p>
        <ul>
          <li><code>unlink &lt;link&gt;</code> or <code>rm &lt;link&gt;</code>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Piping and Redirection</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>file1 | file2</code></b>
      </td>
      <td style="text-align:left">Redirects (STDOUT) <b>output</b> of <em>file 1</em> to (STDIN) <b>input</b> of <em>file 2</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>file1 &gt; file2</code></b>
      </td>
      <td style="text-align:left">
        <p>Saves/redirects the (STDOUT) <b>output</b> of<em> file 1</em> to<em> file 2</em>
        </p>
        <ul>
          <li>Will <b>overwrite</b> the final output each time used</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>file1 &gt;&gt; file2</code></b>
      </td>
      <td style="text-align:left">Appends (STDOUT) <b>output</b> of <em>file 1</em> to<em> file 2 - </em><b>w/o overwriting</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>file1 2&gt; file2</code></b>
      </td>
      <td style="text-align:left">Redirects the (STDERR) <b>error message</b> of <em>file 1</em> to <em>file 2</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>command &lt; file2</code></b>
      </td>
      <td style="text-align:left">Passes the contents of the<em> file 2 </em>(STDIN) to a program</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Shortcuts</b>
      </td>
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + A</code></b> or <b><code>HOME</code></b>
      </td>
      <td style="text-align:left">Moves the cursor to the beginning of the line</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + B</code></b> or &#x21E6;</td>
      <td style="text-align:left">Moves the cursor back one character at a time</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + C</code></b>
      </td>
      <td style="text-align:left">Terminates the current running process</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + D</code></b>
      </td>
      <td style="text-align:left">
        <p>Exits the bash shell - same with <b><code>Exit</code></b> command</p>
        <p>Also removes the character under the cursor while typing</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + E</code></b> or <b><code>END</code></b>
      </td>
      <td style="text-align:left">Moves the cursor to the ending of the line</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + F</code></b> or &#x21E8;</td>
      <td style="text-align:left">Moves the cursor forward one character at a time</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + K</code></b>
      </td>
      <td style="text-align:left">Removes all the text from the cursor until the end of the line</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + L</code></b>
      </td>
      <td style="text-align:left">Clears the terminal (Moves the previous commands up)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + Q</code></b>
      </td>
      <td style="text-align:left">Unfreezes the terminal (<b>doesn&apos;t</b> work in MacOS)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + S</code></b>
      </td>
      <td style="text-align:left">Freezes the terminal (<b>doesn&apos;t</b> work in MacOS)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + X + Backspace</code></b>
      </td>
      <td style="text-align:left">
        <p>Removes all the text from the cursor to the beginning</p>
        <ul>
          <li>Doesn&apos;t work in Mac as there is no backspace
            <ul>
              <li><b><code>Option + Delete</code></b> in MacOS</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL + Z</code></b>
      </td>
      <td style="text-align:left">Pauses the current running process</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL +</code></b>&#x21E6; or <b><code>ALT + B</code></b>
      </td>
      <td style="text-align:left">Moves the cursor back one <b>word</b> at a time</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>CTRL +</code></b>&#x21E6; or <b><code>ALT + C</code></b>
      </td>
      <td style="text-align:left">Moves the cursor forward one <b>word</b> at a time</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>TAB</code></b>
      </td>
      <td style="text-align:left">Use <b><code>TAB</code></b>to auto complete the path/file names</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x21E7; | &#x21E9;</td>
      <td style="text-align:left">Use arrows to display previously typed commands</td>
    </tr>
  </tbody>
</table>

                                                                         **References:**                                                                        

**0\)** [**https://ubuntu.com/tutorials/command-line-for-beginners\#1-overview**](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview)\*\*\*\*

**1\)** [**https://www.pluralsight.com/guides/beginner-linux-navigation-manual**](https://www.pluralsight.com/guides/beginner-linux-navigation-manual)\*\*\*\*

**2\)**  [**https://ryanstutorials.net/linuxtutorial/**](https://ryanstutorials.net/linuxtutorial/)\*\*\*\*

**3\)** [**https://maker.pro/linux/tutorial/basic-linux-commands-for-beginners**](https://maker.pro/linux/tutorial/basic-linux-commands-for-beginners)\*\*\*\*

**4\)** [**https://www.tecmint.com/linux-command-line-bash-shortcut-keys/**](https://www.tecmint.com/linux-command-line-bash-shortcut-keys/)\*\*\*\*

\*\*\*\*

