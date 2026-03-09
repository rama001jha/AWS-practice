<h2>AWS Identity and Access Management (IAM) Basics</h2>

<h3>1. What is an IAM User?</h3>

<p>
In <b>AWS Identity and Access Management (IAM)</b>, an <b>IAM User</b> is a person or application that is given permission to access AWS resources.
</p>

<p>
Instead of using the main AWS account (root user) for daily tasks, administrators create separate IAM users for each person.
</p>

<p><b>Example:</b></p>

<ul>
<li>Developer</li>
<li>DevOps Engineer</li>
<li>Data Analyst</li>
</ul>

<p>
Each user gets their own login credentials and only the permissions they need.
</p>

<p><b>Simple Definition:</b></p>

<p>
An IAM user is a <b>person or application that can log in and use AWS services with specific permissions</b>.
</p>

<hr>

<h3>2. What is an IAM Group?</h3>

<p>
An <b>IAM Group</b> is a collection of IAM users who share the same permissions.
</p>

<p>
Instead of assigning permissions to each user individually, administrators create a group and assign permissions to the group.
</p>

<p><b>Example:</b></p>

<ul>
<li>Developers Group</li>
<li>DevOps Group</li>
<li>Analytics Group</li>
</ul>

<p>
All users inside the group automatically inherit the permissions assigned to that group.
</p>

<p><b>Simple Definition:</b></p>

<p>
An IAM group is a <b>collection of users that share the same permissions</b>.
</p>

<hr>

<h3>3. What is an IAM Policy?</h3>

<p>
An <b>IAM Policy</b> is a set of rules that defines what actions are allowed or denied in AWS.
</p>

<p>
Policies control what users, groups, or roles can do with AWS resources.
</p>

<p><b>Example Permissions:</b></p>

<ul>
<li>Start an EC2 instance</li>
<li>Stop an EC2 instance</li>
<li>Read files from S3</li>
<li>Deny deleting resources</li>
</ul>

<p>
Policies are written in JSON format and are attached to users, groups, or roles.
</p>

<p><b>Simple Definition:</b></p>

<p>
An IAM policy is a <b>set of permissions that controls what actions can be performed in AWS</b>.
</p>

<hr>

<h3>4. What is an IAM Role?</h3>

<p>
An <b>IAM Role</b> provides temporary permissions to users or AWS services to access AWS resources.
</p>

<p>
Unlike IAM users, roles do not have permanent login credentials. They are assumed temporarily when needed.
</p>

<p><b>Example:</b></p>

<p>
An EC2 instance needs permission to access files stored in S3.
</p>

<p>
Instead of storing credentials in the application code, we attach an IAM role to the EC2 instance that allows access to S3.
</p>

<p><b>Simple Definition:</b></p>

<p>
An IAM role is a <b>temporary set of permissions that users or AWS services can assume to access AWS resources</b>.
</p>

<hr>

<h3>Quick Summary</h3>

<table border="1" cellpadding="8">
<tr>
<th>Concept</th>
<th>Meaning</th>
</tr>

<tr>
<td>IAM User</td>
<td>A person or application that can log in and access AWS</td>
</tr>

<tr>
<td>IAM Group</td>
<td>A collection of users with the same permissions</td>
</tr>

<tr>
<td>IAM Policy</td>
<td>A set of rules that defines permissions</td>
</tr>

<tr>
<td>IAM Role</td>
<td>Temporary permissions that can be assumed when needed</td>
</tr>

</table>

<hr>

<p>
These IAM concepts are fundamental for managing access and security in AWS environments.
</p>
