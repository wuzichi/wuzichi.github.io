---
layout: page
title: Search
---

<!-- HTML elements for search -->
<p class="copyright text-muted">
请在搜索前刷新本页清除缓存，否则可能出现搜索错误或者找不到文章
</p>

<input type="text" id="search-input" placeholder="搜索博客 - 输入标题/相关内容/日期/Tags.." style="width:300px;"/>
<ul id="results-container"></ul>

<!-- script pointing to jekyll-search.js -->
<script src="/js/simple-jekyll-search.min.js"></script>

<script>
SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '/search.json',
    searchResultTemplate: '<li><a href="{url}" title="{desc}">{title}</a></li>',
    noResultsText: '没有搜索到文章',
    limit: 20,
    fuzzy: false
  })
</script>
