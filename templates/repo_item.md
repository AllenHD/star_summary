### {{ repo.language | language_emoji }} [{{ repo.name }}]({{ repo.html_url }})

{% if repo.description %}
{{ repo.description | truncate_desc(200) }}
{% else %}
*暂无描述*
{% endif %}

**⭐ 星标:** {{ repo.stargazers_count | format_number }} | **🍴 Fork:** {{ repo.forks_count | format_number }} | **语言:** {{ repo.language or '未知' }}

{% if repo.topics %}
**🏷️ 标签:** {% for topic in repo.topics %}`{{ topic }}`{% if not loop.last %} {% endif %}{% endfor %}
{% endif %}

{% if repo.homepage %}
**🏠 主页:** [{{ repo.homepage }}]({{ repo.homepage }})
{% endif %}

**📅 更新时间:** {{ repo.updated_at | format_date }}
