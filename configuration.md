# Configuration

{% hint style="warning" %}
Theme's newest configuration file can be found in [exampleSite/config.toml](https://github.com/CaiJimmy/hugo-theme-stack/blob/master/exampleSite/config.toml).   
Take that file as reference, this page's content might be outdated.
{% endhint %}

Theme's example configuration is placed under `params` section of `exampleSite/config.toml`.

## Site-wide settings

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>mainSections</code>
      </td>
      <td style="text-align:left">
        <p>Pages places under this/those sections will be shown on homepage and archive
          page.</p>
        <p>Ref: <a href="https://gohugo.io/content-management/sections/">Content Sections</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>featuredImageField</code>
      </td>
      <td style="text-align:left">
        <p>Front Matter <b>field</b> used to fetch featured image of a page. Default <code>image</code>.</p>
        <p><em>Better not to edit this.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rssFullContent</code>
      </td>
      <td style="text-align:left">Output page&apos;s full content in RSS.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>dateFormat</code>
      </td>
      <td style="text-align:left">Date format setting. Notice that Go&apos;s date format is slightly different
        than other programming language, take a look at official documentation:
        <a
        href="https://gohugo.io/functions/dateformat/">dateFormat</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>dateFormat.published</code>
      </td>
      <td style="text-align:left">Page publish date format</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>dateFormat.lastUpdated</code>
      </td>
      <td style="text-align:left">Page last updated date format</td>
    </tr>
  </tbody>
</table>

## Sidebar

Settings related with left-side sidebar.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>avatar</code>
      </td>
      <td style="text-align:left">
        <p>Site owner avatar.</p>
        <p><b>Place image under Hugo site&apos;s <code>assets/img</code> folder.</b>
        </p>
        <p>For example, if the avatar is placed under <code>assets/img/avatar.png</code>,
          then introduce <code>img/avatar.png</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>emoji</code>
      </td>
      <td style="text-align:left">Emoji that appears on bottom of the avatar. Can be empty.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>subtitle</code>
      </td>
      <td style="text-align:left">Site description</td>
    </tr>
  </tbody>
</table>

## Article

Setting related with article page.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>article.license</code>
      </td>
      <td style="text-align:left">
        <p>Article license settings. It shows at the end of article:</p>
        <p></p>
        <ul>
          <li><code>enabled</code>&#xFF1A; Show copyright info under every article by
            default if it&apos;s set to <code>true</code>. Can be disabled individually
            by specifying <code>license: false</code> in article&apos;s Front Matter.</li>
          <li><code>default</code>&#xFF1A; Default article license. Can be overwritten
            by specifying <code>license: &quot;My custom licence&quot;</code> on article&apos;s
            Front Matter.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Comments

Comment system related settings

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">enabled</td>
      <td style="text-align:left">Show comment system by default in every article page.</td>
    </tr>
    <tr>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">
        <p>Comment system provider. Available options:</p>
        <ul>
          <li><code>disqus</code>
            <ul>
              <li>It&apos;s necessary to set <code>disqusShortname</code> field in <code>config.toml</code>.
                Official documentation: <a href="https://gohugo.io/content-management/comments/#configure-disqus">Configure Disqus</a>
              </li>
            </ul>
          </li>
          <li><code>utterances</code>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
To add support for more comment system, create `{provider}.html` under `layouts/partials/comments/provider/`.
{% endhint %}

## **Widgets**

Settings related with right-sidebar widgets.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>widgets.enabled</code>
      </td>
      <td style="text-align:left">
        <p>An array including enabled widget&apos;s name. Available values:</p>
        <ul>
          <li><code>archives</code>: Archives list</li>
          <li><code>tag-cloud</code>: Tag cloud</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>widgets.archives</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><code>limit</code>: How many items are being shown</li>
          <li><code>path</code>: Relative path to archive page. For example <code>/archives</code>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>widgets.tagCloud</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><code>limit</code>: How many items are being shown</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Opengraph

[Open Graph](https://ogp.me/) related settings.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>opengraph.twitter</code>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li><code>site</code>: Site owner&apos;s Twitter username</li>
          <li><code>card</code>: <a href="https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/abouts-cards">Twitter Card Style</a>,
            available values: <code>summary</code> / <code>summary_large_image</code>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Default Image

Default featured image settings \(in case page doesn't have `image` field set in Front Matter.\)

| Name | Description |
| :--- | :--- |
| `defaultImage.opengraph` | Default image for Open Graph tag |

All of those sections has following structure:

* `enabled`
* `src`: Image source
* `local`: If it's `true`, Hugo will look for `src` under your site's `assets` folder.

{% hint style="info" %}
**It's recommended to place images locally**. Otherwise, this theme won't be able to crop and optimize it automatically.
{% endhint %}
