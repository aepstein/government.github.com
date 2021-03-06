---
title: Who's using GitHub?
layout: support-page
description: Government agencies at the national, state, and local level use GitHub to share and collaborate. If you don't see your organization on this list, follow the instructions below to add it!
permalink: /community/
---
<div id="to-top" class="container">
  <div class="row-fluid">
    <div class="span8">
    <div class="search-section">
    <h5><input id="filter" type="text" class="form-control" placeholder="Type to search..."> or jump to <a href="#civichackers">Civic Hackers</a> list.</h5></div>
      <h2 id="governments">Governments</h2>
      <h6 class="govtable no-matches" style="display: none;">No matches.</h6>
        <table class="govtable table">
          <tbody class="searchable">
            <tr class="govtable table-header"><th>Avatar</th><th>Account</th><th>Affiliation</th></tr>
            {% for type_hash in site.data.governments %}
            <tr class="type-block" id="{{ type_hash[0] | downcase | replace: ' ','_' }}">
              <td><h3>{{ type_hash[0] }}</h3></td><td></td><td></td>
            </tr>
            {% for org in type_hash[1] %}
            <tr>
              <td>
                <a href="https://github.com/{{ org }}" title="{{ org }}">
                <img src="https://github.com/{{ org }}.png" width="40" height="40" alt="{{ org }}"></a>
              </td>
              <td>
                <p><a href="https://github.com/{{ org }}" title="{{ org }}">{{ org }}</a></p>
              </td>
              <td>
                <p class="dim-affiliation">{{ type_hash[0] }}</p>
              </td>
            </tr>
          {% endfor %}
          {% endfor %}
        </tbody>
      </table>
    </div>
  </div>

  <div class="row-fluid">
    <div class="span8">
      <h5 id="civichackers" class="search-section">Jump to <a href="#to-top">top</a> or <a href="#governments">Governments</a> list.</h5>
      <h2>Civic Hackers</h2>
      <h6 class="civictable no-matches" style="display: none;">No matches.</h6>
      <table class="civictable table">
        <tbody class="searchable">
          <tr class="civictable table-header"><th>Avatar</th><th>Account</th><th>Affiliation</th></tr>
          {% for type_hash in site.data.civic_hackers %}
          {% unless type_hash[0] == "Civic Hackers" %}
          {% endunless %}
          <tr class="type-block" id="{{ type_hash[0] | downcase | replace: ' ','_' }}">
            <td><h3>{{ type_hash[0] }}</h3></td><td></td><td></td>
            </tr>
            {% for org in type_hash[1] %}
            <tr>
              <td>
                <a href="https://github.com/{{ org }}" title="{{ org }}">
                <img src="https://github.com/{{ org }}.png" width="40" height="40" alt="{{ org }}"></a>
              </td>
              <td>
                <p><a href="https://github.com/{{ org }}" title="{{ org }}">{{ org }}</a></p>
              </td>
              <td>
                <p class="dim-affiliation">{{ type_hash[0] }}</p>
              </td>
            </tr>
            {% endfor %}
          {% endfor %}
        </tbody>
      </table>
    </div>
  </div>

  <div class="row-fluid section">
    <div class="span6" markdown="1">

## Add An Organization to the List

This website is [open source](https://github.com/github/government.github.com), therefore anyone in the community can submit edits through pull requests. If your agency isn't on this list, but should be, please add it:

* Log in to [GitHub](https://github.com){:target="_blank"}.
* Go to [this repository](https://github.com/github/government.github.com) and fork it (button to the top right of the page).
* In your forked version, click the branch dropdown and in the "Find or create a branch..." field, create a new branch (for example, "adding myagencyname").
* Still in your forked version, click on the `_data/governments.yml` file or `_data/civic_hackers.yml` depending on where your organization fits.
* At the top of the file is a list of the organizations populating this page. Click edit, near the top right, and then add your organization's GitHub account name just like the others: `- GroupGithubOrg`.
* Click Commit Changes at the bottom of the page.
* Visit the [original repository](https://github.com/github/government.github.com) and select Compare & pull request.
* Fill out the form and click Send pull request!

### Guidelines

While there are many many interesting government-related projects, we are limiting the list above to [GitHub organizations](https://help.github.com/articles/user-organization-and-project-pages) with projects on GitHub, who are:

* Official government institutions, listed under their country or level of government
* Non-profits or groups focused on government, listed under "Civic Hackers"

</div>
</div>

  <div class="row-fluid section">
    <div class="span6 fine-print">
      <small markdown="1">
Neither the inclusion of a logo or seal above nor the fact that a particular government entity may have a presence on GitHub.com should be construed to imply that GitHub's products or services are endorsed, sponsored or recommended by the government entity, nor that they are considered by that entity to be superior to any other products or services. If you have any questions, or if would like your agency's logo removed from the list above, please [let us know](https://github.com/github/government.github.com/issues/new){: data-proofer-ignore="true"}.
      </small>
    </div>
  </div>
</div>
