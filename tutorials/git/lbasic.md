---
description: >-
  Some of the most common Linux commands and their usages listed in the table
  below.
---

# Linux / Shell Basics

<table>
  <thead>
    <tr>
      <th style="text-align:left">Command Type</th>
      <th style="text-align:left">Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Navigation Commands</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>pwd</code></b>
      </td>
      <td style="text-align:left">Prints working directory</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cd &lt;dir&gt;</code></b>
      </td>
      <td style="text-align:left">Changes directory to given directory (folder)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>ls &lt;dir&gt;</code></b>
      </td>
      <td style="text-align:left">Lists all the files in given / current directory</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>man &lt;command&gt;</code></b>
      </td>
      <td style="text-align:left">Opens the manual for the given command</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>&lt;command&gt; --help</code></b>
      </td>
      <td style="text-align:left">Opens the help page for the given command</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>time &lt;command&gt;</code></b>
      </td>
      <td style="text-align:left">Prints the time takes to execute the given command</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>date</code></b>
      </td>
      <td style="text-align:left">Prints the full date</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>du</code></b>
      </td>
      <td style="text-align:left">Shows disk usage</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>df</code></b>
      </td>
      <td style="text-align:left">Shows a report on the disk space usage</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cat</code></b>
      </td>
      <td style="text-align:left">Concatenate - Multiple purpose</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>shutdown &lt;time&gt;</code></b>
      </td>
      <td style="text-align:left">Shuts down the system at a given time</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>reboot</code></b>
      </td>
      <td style="text-align:left">Stops and restarts the system</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>exit</code></b>
      </td>
      <td style="text-align:left">Logs out of terminal (Ctrl+D)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Displaying File Contents</b>
      </td>
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>echo &lt;&quot;string&quot;&gt;</code></b>
      </td>
      <td style="text-align:left">Prints the given string</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cat &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">Prints the contents of the given file</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>less &lt;file&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Displays the contents of the given file</p>
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
      <td style="text-align:left">Searches for <b>content </b>in the text file</td>
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
              <li><b><code>mv &lt;file_name&gt; &lt;new_name&gt;</code></b>
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
          <li>Can<b>not</b> remove directories unless used with <b><code>-r</code></b> option
            <ul>
              <li><b><code>rm -r &lt;dir&gt;</code></b>- <b>Recursively</b> deletes all files
                in dir</li>
              <li><b><code>rm -rf &lt;dir&gt;</code></b> - Does <b>not</b> ask for permit</li>
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
      <td style="text-align:left">Creates a new file or files</td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>cp &lt;file&gt; &lt;new_name&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Copies the given file with a given new name</p>
        <ul>
          <li>Can copy directories <b>recursively</b> with <b><code>-r</code></b> option
            <ul>
              <li><b><code>cp -r &lt;dir&gt; &lt;new_name&gt;</code></b>
              </li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b><code>ln &lt;source&gt; &lt;link&gt;</code></b>
      </td>
      <td style="text-align:left">
        <p>Creates hard / symbolic (<b><code>-s</code></b> option) links between files
          <br
          />In order to remove the symbolic links use either:</p>
        <ul>
          <li><b><code>unlink &lt;link&gt;</code></b> or <b><code>rm &lt;link&gt;</code></b>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;code&gt;&lt;/code&gt;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

