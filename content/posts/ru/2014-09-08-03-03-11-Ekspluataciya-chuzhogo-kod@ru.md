---
$title@: Ekspluataciya-chuzhogo-koda
author@: Viktor Zharina
$order: 194
$dates:
  published: 2014-09-08 03:03:11
---
<h2>Введение</h2>

В данном посте я опишу ситуацию, в которой по каким-либо причинам мне передавали чужой проект и он становился моим. Мой опыт связан с изменением места работы. Я переходил в другую компанию, в которой уже было программное обеспечение. ПО нуждалось в поддержке, в доработке. Ниже я дам описание и советы, которые, возможно, облегчат кому-нибудь жизнь и и сберегут выходные.

<h2>Не ссы!</h2>

Это универсальный совет на все случаи жизни. Это совет я часто даю сам себе и в целом привык к нему. В контексте поста он значит то, что скорее всего вы, как программист-разработчик столкнетесь с большим количеством кода и, скорее всего, этот код будет не очень хорошего качества. Еще очень вероятно, что не будет документации. Я сталкивался и сталкиваюсь с тем, что ее почти нет. Так вот: "Не ссы!". Первые пару месяцев (иногда больше) есть время на изучение, есть время и возможность сказать: "Я недавно работаю, объясните мне" и т.д. Вторым моментом является то, что раз вас наняли, значит компания готова нести риски и первое время платить вам за ваше обучение. Тратьте это время с пользой для себя и для компании, изучайте бизнес-процессы, изучайте код, отмечайте где его можно улучшить без большого ущерба для себя и для системы.

<h2>Определите состояние дел</h2>

1) Есть ли система контроля версий, либо как выполняется обновление?



2) Есть ли тестовая система, к которой имеют доступ пользователи, которые эксплуатириуют программное обеспечение?



3) Реквизиты доступа, версии по, бекапы, настройки.



4) Как разрабатывали и поддерживали ПО до вас?

<h2>Начало работ</h2>

Скорее всего дадут какую-то несложную задачу без лимита по времени. Если все нормально с квалификацией, то проблем быть не должно. На протяжении выполнения подобных задач и сталкиваясь с какими-то трудностями ищите подобные решения в самом проекте. Скорее всего то, что вы делаете уже кто-то делал до вас. Причем нужно стараться делать именно так, как было сделано до этого, иначе вас не поймут.



Если вдруг наткнулись на крайне запутанный метод и вам нужно внестив него изменения не торопитесь это делать. Локализуйте место внесения изменений, проконтролируйте как ваши изменения повлияют на код, который идут ниже вашего, протестируйте на своей машине, протестируйте на пользователях.



И хотелось бы добавить, что вам не избежать говнокода, при условии, что вас будут спрашивать о сроках. Компании нужен результат, а не качественный код. Ищите свободное время и улучшайте качество кода самостоятельно, для себя, для упрощения жизни себе и другим.



Если вас спрашивают о сроках завершения оцените примерно умножьте на 2 и сообщите. Сообщайте всегда минимальное и максимальное время, так как велика неопределенность.

<h2>Уже втянулись</h2>

Улучшайте код, договоритесь о стандарте кодирования, оформляйте код по стандарту. Часто вас будут торопить с выполнением задач и иногда будет нужно сделать лишь бы работало, так вот делайте, но потом исправляйте, обязательно исправляйте. Пишите тесты, ведь они залог уверенности. Пишите документацию, заметки, faq.



&nbsp;



&nbsp;