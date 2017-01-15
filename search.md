---
layout: home
---
<ul id="post-list" data-search-results></ul>
<script type="text/x-template" id="search-result">
    <li class="post-item post">
        <a href="##Url##">
            <h3 class="post-title">##Title##</h3>
            <p class="post-excerpt">##Content##</p>
        </a>
        <p class="post-tags">##Tags##</p>
            <div class="post-meta">
                <a href="##AuthorUrl##">
                    <div class="author-image" style="background-image:url(##AuthorImage##);">
                        <span class="sr-only">##AuthorName##'s profile image</span>
                    </div>
                    <p class="author-name">##AuthorName##</p>
                </a>
                <p class="post-date">##Date##</p>
            </div>
    </li>
</script>

<!--
https://github.com/christian-fei/Simple-Jekyll-Search
-->