---
layout: default
title: Página Inicial
---

<div style="max-width: 800px; margin: 0 auto; padding: 20px;">
    <h1>📰 Minhas Últimas Postagens</h1>
    <p>Bem-vindo ao meu blog. Confira o que eu escrevi:</p>

    <hr>

    <ul style="list-style: none; padding: 0;">
        {% for post in site.posts %}
            <li style="margin-bottom: 30px; border-bottom: 1px solid #eee; padding-bottom: 20px;">
                <span style="font-size: 0.8rem; color: #666;">{{ post.date | date: "%d/%m/%Y" }}</span>
                
                <h2 style="margin: 5px 0;">
                    <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: #2563eb;">
                        {{ post.title }}
                    </a>
                </h2>
                
                <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
                
                <a href="{{ post.url | relative_url }}" style="font-weight: bold; color: #000;">Ler mais →</a>
            </li>
        {% endfor %}
    </ul>
</div>
