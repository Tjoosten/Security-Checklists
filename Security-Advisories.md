# Security risk levels defined 

The following information explains how the criticality level as a general guideline for determining 
security risk levels. 

<h2>Risk Calculator</h2>

The current security advisory risk level system is based on the <a href='http://www.nist.gov/itl/csd/cmss-072512.cfm'>NIST Common Misuse Scoring System (NISTIR 7864)</a>. Each vulnerability is scored using this system and a number is assigned between 0 and 25. The total points are used to give a text description to make the numbers easier to understand:
<ul>
<li>scores between 0 and 4 are considered Not Critical</li>
<li>5 to 9 is considered Less Critical</li>
<li>10 to 14 is considered Moderately Critical</li>
<li>15 to 19 is considered Critical</li>
<li>20 to 25 is considered Highly Critical</li>
</ul>

The risk level is assigned by the <a href="https://security.drupal.org/riskcalc">Risk Calculator</a> which takes 6 different metrics, each which can have 3 different values. This is encoded in a terse format and included on every Security Advisory in the "Security risk" field. The below table provides longer descriptions and point scores for each category.

<table>
<caption>Risk metrics used</caption>
<thead>
<tr>
<th>Code</th>
<th>Metric</th>
<th>Description</th>
</tr>
</thead>
</tbody>
<tr>
<td>AC</td>
<td>Access complexity</td>
<td>
<p><strong>How difficult is it for the attacker to leverage the vulnerability?</strong></p>
<ul>
<li>AC:None = None (user visits page) +4 points</li>
<li>AC:Basic = Basic or routine (user must follow specific path) +2 points</li>
<li>AC:Complex = Complex or highly specific (multi-step, unintuitive process with high number of dependencies) +1 point</li>
</ul>
</td>
</tr>
<tr>
<td>A</td>
<td>Authentication</td>
<td>
<p><strong>What privilege level is required for an exploit to be successful?</strong></p>
<ul>
<li>A:None = None (all/anonymous users) +4 points</li>
<li>A:User = User-level access (basic/commonly assigned permissions) +2 points</li>
<li>A:Admin = Administrator (broad permissions required where 'restrict access' is set to false) +1 point</li>
</ul>
</td>
</tr>
<tr>
<td>CI</td>
<td>Confidentiality impact</td>
<td>
<p><strong>Does this vulnerability cause non-public data to be accessible?</strong></p>
<ul>
<li>CI:All = All non-public data is accessible +5 points</li>
<li>CI:Some = Certain non-public data is released +3 points</li>
<li>CI:None = No confidentiality impact +0 points</li>
</ul>
</td>
</tr>
<tr>
<td>II</td>
<td>Integrity impact</td>
<td>
<p><strong>Can this exploit allow system data (or data handled by the system) to be compromised?</strong></p>
<ul>
<li>II:All = All data can be modified or deleted +5 points</li>
<li>II:Some = Some data can be modified +3 points</li>
<li>II:None = Data integrity remains intact +0 points</li>
</ul>
</td>
</tr>
<tr>
<td>E</td>
<td>Exploit (Zero-day impact)</td>
<td>
<p><strong>Does a known exploit exist?</strong></p>
<ul>
<li>E:Exploit = Exploit exists (documented or deployed exploit code already in the wild) +3 points</li>
<li>E:Proof = Proof of concept exists (documented methods for developing exploit exist in the wild) +2 points</li>
<li>E:Theoretical = Theoretical or white-hat (no public exploit code or documentation on development exists) +1 point</li>
</ul>
</td>
</tr>
<tr>
<td>TD</td>
<td>Target distribution</td>
<td>
<p><strong>What percentage of users are affected?</strong></p>
<ul>
<li>TD:All = All module configurations are exploitable</li>
<li>TD:Default = Default or common module configurations are exploitable, but a config change can disable the exploit</li>
<li>TD:Uncommon = Only uncommon module configurations are exploitable</li>
</ul>
</td>
</tr>
</tbody>
</table>

<h2>External resources</h2>

<ul>
<li><a href="http://mydropninja.com/blog/understanding-drupal-security-advisories-risk-calculator">Understanding Drupal Security Advisories: The Risk Calculator</a>: an article by <a href="https://www.drupal.org/u/dsnopek">David Snopek</a> (a member of the Drupal Security Team)</li>
</ul>


<h2>Risk levels for advisories prior to Summer 2014</h2>

<table>
<thead>
<tr>
<th>Risk Level</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Highly Critical</strong></td>

<td>Remotely exploitable vulnerabilities that can compromise the system. Interaction is not normally required for this exploit to be successful. Exploits have occurred to systems.

Previous examples include: Local file inclusion on Windows, Impersonation, privilege escalation
</td>
</tr>

<tr>
<td><strong>Critical</strong></td>
<td>Remotely exploitable Denial of Service (DOS) vulnerabilities that can compromise the system but do require user interaction.  Vulnerabilities that may allow anonymous users (i.e. users not registered at the site) to log in as a site user or take administrative actions.   Interaction (such as an administrator viewing a particular page) may be required for this exploit to be successful, or in cases where interaction is not required (such as CSRF) the exploit causes only minor damage.

Previous examples include: OpenID impersonation, SQL injection
</td>
</tr>

<tr>

<tr>
<td><strong>Moderately Critical</strong></td>

<td>Remotely exploitable vulnerabilities that can compromise the system.  Interaction (such as an administrator viewing a particular page) is required for this exploit to be successful.  Exploits have not yet occurred on systems when vulnerability was disclosed.  The exploit requires the user to be registered at the site and have some non-default permission, such as creating content.

Previous examples include: Cross Site Scripting, Access bypass
</td>
</tr>

<td><strong>Less Critical</strong></td>

<td>Used for cross-site request forgery vulnerabilities as well as privilege escalation vulnerabilities which require complex chains of events.
This rating also includes vulnerabilities which might expose sensitive data to local users.

Previous examples include: Session fixation, Cross site request forgery

</td>
</tr>

<tr>
<td><strong>Not Critical</strong></td>

<td>Rating is used for limited privilege escalation vulnerabilities and local Denial of Service (DOS) vulnerabilities.

Previous examples include: Access bypass, Failure to encrypt data
</td>
</tr>
</tbody>
</table>
