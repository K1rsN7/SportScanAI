<div align="center">
    <h1>SportScanAI</h1>
    <a href="https://github.com/K1rsN7/BusinessLunchGAN/issues">
        <img src="https://img.shields.io/github/issues/K1rsN7/BusinessLunchGAN?color=4A73DF&labelColor=1C2325&style=for-the-badge" alt="Issues">
    </a>
    <a href="https://github.com/K1rsN7/BusinessLunchGAN/stargazers">
        <img src="https://img.shields.io/github/stars/K1rsN7/BusinessLunchGAN?color=4A73DF&labelColor=1C2325&style=for-the-badge" alt="Stars">
    </a>
    <a href="./LICENSE">
        <img src="https://img.shields.io/badge/Licence-CC%20BY--NC%204.0-4A73DF?style=for-the-badge&labelColor=1C2325" alt="Лицензия CC BY-NC 4.0">
    </a>
</div>
    <p>В мобильном приложении <a href="https://мойфитнес.рф/">МойФитнес</a> проходит много соревнований по шагам и тренировкам.</p>
    <p>Данные о шагах и физической активности приходят от внешних вендоров, в том числе могут собирать шаги с шагомера, встроенного в смартфон.</p>
    <p>Однако, чтобы победить, пользователи становятся крайне изобретательны. Они трясут смартфоном сидя в офисе, крепят его на маятник в часах с кукушкой, привязывают к игривой собаке и т.д. — что только не делают люди, чтобы победить в соревновании по шагам! И это чистой воды “читерство”.</p>
    <p>Цель нашего проекта — разработать алгоритм, который определяет вероятность читерства во время тренировок. Выявление таких "мошенников" представляет собой сложную задачу, поэтому для поддержания честности необходим искусственный интеллект.</p>
    <p>Как допинг портит реальный спорт, так и жульничество подрывает дух виртуальных соревнований. Чтобы поддержать справедливость и сохранить суть спортивного мастерства, борьба с мошенниками приобретает первостепенное значение.</p>
    <strong>Давайте же начнем ловить этих читеров!</strong>

<h2 align="center">Модель</h2>
<div align="center">
    <p>Модель CatBoost вы можете скачать из <a href="https://github.com/DIMFLIX-OFFICIAL/SportScanAI/releases/tag/v1.0.0">релизов</a> с тегом v1.0.0.</p>
</div>

<h2 align="center">Docker</h2>
<h3 align="center">Ссылка на готовый Docker образ</h3>
<div align="center">
    <p><a href="https://hub.docker.com/repository/docker/dimflix/sport-scan-ai:latest">https://hub.docker.com/repository/docker/dimflix/sport-scan-ai:latest</a></p>
</div>

<h3 align="center">Основные команды</h3>
    <ul>
        <li><strong>Build Docker образа:</strong><br><code>docker build -t sport-scan-ai .</code></li>
        <li><strong>Запуск Docker образа:</strong><br><code>docker run --rm --mount type=bind,source="$(pwd)/input-sample.json",target=/input.json sport-scan-ai</code></li>
        <li><strong>Запуск Docker образа без предварительной установки:</strong><br><code>docker run --rm --mount type=bind,source="$(pwd)/input-sample.json",target=/input.json dimflix/sport-scan-ai:latest</code></li>
        <li><strong>Сборка образа в архив и сохранение:</strong><br><code>docker save sport-scan-ai:latest -o sport-scan-ai.tar</code></li>
        <li><strong>Загрузка образа из архива:</strong><br><code>docker load -i sport-scan-ai.tar</code></li>
        <li><strong>Обновить образ на Docker Hub:</strong><br>
            <code>docker build -t &lt;username&gt;/&lt;image-name&gt;:latest .</code><br>
            <code>docker login</code><br>
            <code>docker push &lt;username&gt;/&lt;image-name&gt;:latest</code>
        </li>
    </ul>

<h2 align="center">Авторы</h2>
<table align="center">
  <tr>
    <td align="center">
      <a href="https://github.com/DIMFLIX-OFFICIAL">
        <img src="https://github.com/DIMFLIX-OFFICIAL.png?size=100" width="100px;" alt="" /><br />
        <b>Пронин Дмитрий</b>
      </a><br />
      <sub>Построение и оптимизация алгоритмов. Настройка Docker</sub>
    </td>
    <td align="center">
      <a href="https://github.com/K1rsn7">
        <img src="https://github.com/K1rsn7.png?size=100" width="100px;" alt="" /><br />
        <b>Кирилл Сухоруков</b>
      </a><br />
      <sub>Построение алгоритмов. Обучение модели CatBoost</sub>
    </td>
  </tr>
</table>

<h2 align="center">Лицензия</h2>
    <p>Полный текст лицензии доступен здесь: <a href="https://creativecommons.org/licenses/by-nc/4.0/legalcode">Юридический кодекс CC BY-NC 4.0</a>.</p>
    <h3 align="center">Вы можете свободно использовать:</h3>
    <ul align="center">
        <li>Делиться — копировать и распространять материал на любом носителе или в любом формате.</li>
        <li>Адаптировать — переделывать, преобразовывать и дополнять материал Лицензиар не может лишить вас этих прав, пока вы соблюдаете условия лицензии.</li>
    </ul>
    <h3 align="center">На следующих условиях:</h3>
    <ul align="center">
        <li>Указание авторства — Вы должны предоставить соответствующую информацию, ссылку на лицензию и указать, были ли внесены изменения. Вы можете делать это любым разумным способом, но не таким, который предполагает, что лицензиар одобряет вас или ваше использование.</li>
        <li>Некоммерческий — Вы не имеете права использовать материалы в коммерческих целях.</li>
        <li>Никаких дополнительных ограничений — Вы не имеете права применять юридические условия или технологические меры, которые юридически ограничивают действия других лиц, разрешенные лицензией.</li>
    </ul>
    <p>Это всего лишь краткая выдержка из основных положений лицензии. Пожалуйста, ознакомьтесь с полным юридическим текстом лицензии для полного понимания ее условий.</p>
