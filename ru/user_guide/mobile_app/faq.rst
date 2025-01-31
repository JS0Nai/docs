*******************************************************
Мобильное приложение для Multi-Vendor: Вопросы и ответы
*******************************************************

.. important::

    Мы предлагаем нативное мобильное приложение, чтобы покупатели могли взаимодействовать с вашим маркетплейсом. Приложение написано на React Native и поддерживает устройства на базе Android и iOS.

.. contents::
   :local:

======================
Часть 1. Общие вопросы
======================

--------------
Что это такое?
--------------

У Multi-Vendor адаптивный дизайн. Это значит, что магазин подстраивается под размеры экрана тех устройств, с которых его просматривают. Так покупатели могут оставлять заказы со смартфонов или планшетов.

Но есть и другой способ взаимодействия с магазином — через мобильное приложение. Это программа, которую покупатели устанавливают на свои мобильные устройства. Программа обменивается данными с магазином, так что покупатели могут увидеть, какие есть товары, заказать их, добавить в список желаемого, и т.д.

----------------------------------------------------------------
Зачем нужно приложение, если адаптивный сайт делает то же самое?
----------------------------------------------------------------

* **Приложение заточено под мобильные устройства.** Адаптивный сайт должен нормально выглядеть и работать на любых экранах: и на смартфоне, и на большом мониторе. К мобильному приложению таких требований нет: оно должно работать только на небольших сенсорных экранах.

* **Приложение работает быстрее.** Когда вы просматриваете сайт, вы делаете это через браузер; браузер должен загрузить через интернет все элементы страницы (интерфейс, изображения, и т.д.). Приложение работает иначе: интерфейс уже хранится на вашем устройстве, поэтому приложению нужно загрузить только важные данные (например, новые товары).

* **Приложение — это один из видов рекламы.** Во-первых, логотип магазина (или любое другое изображение на ваш выбор) появится в Apple App Store и в Google Play как иконка приложения. Во-вторых, если покупатель скачает приложение, то эту иконку он будет регулярно видеть на экране смартфона среди других приложений.

  .. fancybox:: img/responsive_vs_mobile.png
      :alt: Мобильное приложение в сравнении с адаптивным сайтом на Multi-Vendor.

.. _mobile-app-faq-sync:

-------------------------------------------------
Как приложение синхронизируется с моим магазином?
-------------------------------------------------

В приложении есть все товары, которые есть у вас в магазине. Если вы добавите или удалите товары, категории, способы доставки или оплаты, то они также появятся или исчезнут из приложения.

Если у покупателя есть учётная запись в магазине, он сможет использовать её и в приложении. При регистрации в приложении покупатель также получает учётную запись в магазине.

Если покупатель добавляет товар в корзину или в список отложенных товаров в приложении, то эти действия переносятся в магазин (и наоборот; синхронизация работает в обе стороны). Заказы из приложения ничем не отличаются от заказов с сайта: вы работаете с ними через панель администратора магазина, а покупатели всегда видят всю историю своих заказов (т.е. заказы и с сайта, и из мобильного приложения).

--------------------------------------------------------
Какие способы доставки и оплаты поддерживает приложение?
--------------------------------------------------------

Приложение поддерживает **все способы доставки** и следующие способы оплаты:

* PayPal Express Checkout;

* Яндекс.Касса;

* Оффлайн-платежи (наподобие "Обсудить с менеджером", и т.п.).

Способы оплаты в мобильном приложении расположены в том же порядке, что и в магазине. По умолчанию выбран первый способ из списка.

.. hint::

    Техническая информация — список поддерживаемых шаблонов способов оплаты: ``cc.tpl``, ``check.tpl``, ``empty.tpl``, ``paypal_express.tpl``, ``phone.tpl``, ``yandex_money.tpl``.
  
.. warning::   

    Мобильное приложение поддерживает модуль :doc:`/user_guide/addons/direct_customer_to_vendor_payments/index` из Multi-Vendor Plus и Ultimate, начиная с версии Multi-Vendor 4.12.3.

------------------------------------
Какие языки поддерживает приложение?
------------------------------------

Пока что приложение поддерживает только английский и русский: если один из этих языков выбран на устройстве, то приложение будет работать на этом языке. На русский и английский мы переводим приложение сами.

Тексты мобильного приложения находятся в Multi-Vendor в модуле **Мобильное приложение**. Когда появится поддержка других языков, то переводы на них будут выполняться сообществом и проверяться нашими партнёрами `в проекте на сервисе CrowdIn <https://crowdin.com/project/cs-cart-latest>`_.

.. fancybox:: img/crowdin_project.png
    :alt: Проект по переводу Multi-Vendor на сервисе CrowdIn.

--------------------------------------
Есть ли в приложении push-уведомления?
--------------------------------------

Да. Если вы их включите, то покупателям будут приходить сообщения на мобильные телефоны об изменениях статусов заказов. Чтобы включить push-уведомления в приложении:

#. Зарегистрируйтесь на `https://firebase.google.com <https://firebase.google.com>`_.

#. Создайте проект для Android и iOS.

#. Введите ключ в настройках модуля **Мобильное приложение**. Модуль идёт в комплекте с Multi-Vendor, но не установлен по умолчанию.

#. Используйте кнопку **Скачать настройки**, чтобы получить архив с настройками приложения.

#. Отправьте нам полученный архив **app_settings.zip**.

----------------------------------------
Могу я получить исходный код приложения?
----------------------------------------

Да, но это зависит от редакции Multi-Vendor edition. Подробности есть `на странице сравнения редакций Multi-Vendor <https://multivendor.cs-cart.ru/#compare>`_.

Для исходного кода мы предоставляем ограниченную техническую поддержку. Лицензионное соглашение позволяет использовать исходный код только с одной установкой Multi-Vendor, а также запрещает публиковать исходный код или передавать его третьим лицам. Зато вы сможете опубликовать приложение из своей учётной записи в Apple App Store и Google Play, чтобы именно ваша компания отображалась как разработчик приложения.

--------------------------------------------
Кто отображается как разработчик приложения?
--------------------------------------------

Если у вас есть исходный код приложения, вы сможете опубликовать его с вашей учётной записи разработчика. В остальных случаях мы сами опубликуем приложение за вас, и тогда у приложения будет следующий разработчик:

* В Apple App Store: `CS-Cart <https://apps.apple.com/ru/developer/cs-cart/id1572599656?see-all=i-phone-apps>`_

* В Google Play: `BOLIDE NETWORK LLC <https://play.google.com/store/apps/developer?id=BOLIDE+NETWORK+LLC>`_


=============================
Часть 2. Получение приложения
=============================

--------------------------------------------------
Можно ли протестировать приложение перед покупкой?
--------------------------------------------------

У нас есть демо-приложение `для Android <https://play.google.com/store/apps/details?id=com.simtech.multivendor>`_ и `для iOS <https://itunes.apple.com/app/multi-vendor-app-by-cs-cart/id1304872157>`_. Оно привязано к демо-магазину на базе Multi-Vendor. Можете установить это приложение себе, походить по каталогу, подобавлять товары в корзину, "заказать" их и т.д. Естественно, мы ничего в демо-магазине взаправду не продаём; демо только показывает, как работает приложение.

-----------------------------------------------------
Как получить мобильное приложение для моего магазина?
-----------------------------------------------------

#. Если вы решите, что вам нужно приложение (или если возникнут какие-то вопросы), свяжитесь с нами через форму `обратной связи <https://www.cs-cart.ru/marketplace/demo>`_.

#. Чтобы создать приложение и опубликовать его в Apple App Store и на Google Play, нам понадобится от вас кое-какая информация.

   В Multi-Vendor встроен модуль **Мобильное приложение** (не установлен по умолчанию). Этот модуль позволяет:

   * Предоставить информацию, необходимую для публикации приложения (тексты, изображения, ссылки, и т.д.).

   * Настроить внешний вид приложения (цвета, логотипы, и т.д.). На этом этапе также можно :ref:`отредактировать тексты мобильного приложения <mobile-app-faq-texts>`.

     .. fancybox:: img/mobile_app_color_editing.png
         :alt: Интерфейс для редактирования цветов в мобильном приложении.

   Модуль сам по себе не создаст вам мобильное приложение. Когда вы зададите и сохраните все настройки, нажмите кнопку **Скачать настройки**. Вы получите архив **app_settings.zip**. Пришлите этот архив нам, и у нас будет вся информация для публикации вашего приложения.

---------------------------------------------------
С какими версиями Multi-Vendor работает приложение?
---------------------------------------------------

Лучше всего использовать самую новую версию. Там всегда самые последние изменения в модуле **Мобильное приложение** и в механизме взаимодействия приложения с магазином.

Если у вас не последняя версия, просто упомяните это при обращении к нам, и мы поможем начать. Например, модуль **Мобильное приложение** впервые появился в версии 4.8.1, но с тех пор мы его улучшили. Поэтому нам может сначала потребоваться перенести эти улучшения на вашу установку Multi-Vendor.

Мобильное приложение также может работать на версиях старше 4.8.x (самая ранняя версия, на которой мы его запускали — 4.6.3), но чем старше версия, тем больше изменений может понадобиться. Мы не обещаем интегрировать мобильное приложение в любую старую версию, но если вы сообщите нам в `Help Desk <https://helpdesk.cs-cart.com>`_ номер вашей версии, то мы изучим такую возможность и сообщим вам о результатах.

---------------------------------------------------
Как скоро после оплаты вы выпустите моё приложение?
---------------------------------------------------

Выпуск мобильного приложения может занять какое-то время. Мы подготовим и загрузим приложение в Google Play и Apple App Store в течение месяца после того, как получим от вас архив **app_settings.zip**.

Если выпуск приложения в Google Play или Apple App Store займёт больше времени, а задержка будет на нашей стороне, мы можем бесплатно продлить вашу подписку. Такие решения принимаются индивидуально, и для этого нужно обращаться в `Help Desk <https://helpdesk.cs-cart.com>`_.

---------------------------------------------------------
Какие данные вам нужны для выпуска мобильного приложения?
---------------------------------------------------------

Большую часть этих данных нужно предоставить нам через модуль **Мобильное приложение** (вместе с цветами будущего приложения):

#. **Изображения:**

   * *Иконка приложения* — картинка с размером 1024x1024, которая будет логотипом вашего приложения. Такой большой размер обусловлен требованиями Apple; обязательно проверьте, что эта же картинка хорошо смотрится, если уменьшить размер до 256x256.

   * *Картинка для описания* — изображение с размером 1024x500, которое появится на странице вашего приложения в Google Play. Подробнее читайте в `инструкциях Google Play <https://support.google.com/googleplay/android-developer/answer/1078870?hl=ru>`_ (см. *Картинка для раздела "Рекомендуемые"*).

   * *Заставка* — изображение в двух вариантах (вертикальное 1536x2208 и горизонтальное 2208x1536). Заставка будет отображаться при запуске приложения на мобильном устройстве.

     .. note::

         В Apple App Store и Google Play не принимаются изображения с прозрачным фоном (т.е. с альфа-каналом). Поэтому уберите альфа-канал перед загрузкой изображений. Самый простой способ это сделать — открыть изображение и сохранить его в формате JPG. В PNG-картинках альфа-канал может быть или не быть, а в JPG его точно нет.

#. **Информация о приложении:**

   * *Название приложения* — до 30 символов.

   * *Краткое описание приложения* — до 80 символов.

   * *Полное описание приложения* — до 4000 символов.

#. **Ваша контактная информация:**

   * *Email поддержки* — электронный адрес, по которому покупатели будут слать вам отзывы о приложении. Этот адрес появится на странице приложения в Google Play и Apple App Store.

   * *Ссылка на политику конфиденциальности* — ссылка на страницу вашего магазина, где находится ваша политика конфиденциальности.

.. important::

    Перед тем, как мы выпустим приложение в Google Play и Apple App Store, мы предоставим вам тестовое приложение либо для Android, либо для iOS. В зависимости от того, на какой системе вы хотите его протестировать, пришлите нам ваш электронный адрес либо от Google Play, либо от Apple App Store.

.. fancybox:: img/mobile_app_general_settings.png
    :alt: Интерфейс для редактирования изображений и описаний мобильного приложения.


================================
Часть 3. Изменения после выпуска
================================

--------------------------------------------------
Что я смогу изменить в своём мобильном приложении?
--------------------------------------------------

После того, как приложение выпущено, оно будет автоматически :ref:`обмениваться данными с магазином <mobile-app-faq-sync>`. Но вы также можете внести изменения во внешний вид магазина без нашей помощи и без необходимости для ваших покупателей обновлять приложение. Вот что вы можете изменить:

#. **Содержимое домашней страницы.** Вы можете добавить туда :doc:`блоки </user_guide/look_and_feel/layouts/blocks/index>` 5 разных типов:

   * Баннеры

   * Категории

   * Продавцы

   * Товары

   * Страницы

     .. fancybox:: img/mobile_app_layout.png
         :alt: Редактор цветов мобильного приложения.

#. **Ссылки в нижнем меню боковой панели.** Верхнее боковое меню (с иконками) всегда остаётся неизменным, а нижнее меню можно настраивать: добавлять и удалять оттуда пункты.

   .. important::

       Изменять домашнюю страницу и боковое меню нужно в панели администратора магазина. Откройте страницу **Дизайн → Макеты** и переключитесь на макет **MobileAppLayout**. Он появится только при установленном модуле **Мобильное приложение**.

------------------------------------------------------------------------------------------
Как быть, если я хочу изменить цвета или логотипы после того, как приложение опубликовано?
------------------------------------------------------------------------------------------

Если вы внесёте изменения в настройки модуля **Мобильное приложение** (например, измените цвета или включите push-уведомления), то эти изменения не появятся в опубликованном приложении автоматически.

#. Внесите изменения и сохраните их.

#. Нажмите кнопку **Скачать настройки**, чтобы снова получить из модуля архив **app_settings.zip**.

#. Пришлите архив нам, и мы применим изменения.

   .. fancybox:: img/mobile_app_color_editing.png
       :alt: Редактор цветов мобильного приложения.

   .. important::

       У некоторых планов есть ограничения по количеству запросов на изменение приложения (на странице приложения это называется "tweaks on request", т.е. "изменения в приложении по вашему запросу").

.. _mobile-app-faq-texts:

-----------------------------------
Как мне изменить тексты приложения?
-----------------------------------

Тексты приложения являются частью модуля **Мобильное приложение**, и их можно редактировать в панели администратора магазина. Редактирование текстов работает так же, как :doc:`перевод Multi-Vendor </user_guide/look_and_feel/languages/translate>`:

#. Откройте страницу **Языки → Переводы**. 

#. Введите ``mobile_app.mobile_`` в поисковой строке в боковой панели справа — так в результатах поиска будут тексты, которые используются в мобильном приложении.

#. После того, как вы изменили тексты и сохранили свои изменения, скачайте архив **app_settings.zip** из настроек модуля **Мобильное приложение** и пришлите архив нам.

   .. fancybox:: img/mobile_app_texts.png
       :alt: Поиск текстов мобильного приложения в панели администратора Multi-Vendor.

   .. important::

       У некоторых планов есть ограничения по количеству запросов на изменение приложения (на странице приложения это называется "tweaks on request", т.е. "изменения в приложении по вашему запросу").

------------------------------------------------------------
Домашняя страница: Как добавить работающие ссылки в баннеры?
------------------------------------------------------------

Как было сказано выше, на домашней странице в макете **MobileAppLayout** можно создать блок с баннерами. Если на сайте вы могли ввести для баннера URL вида ``https://example.com/category/product`` чтобы сослаться на товар, то в мобильном приложении это не сработает: приложение не использует ссылки для обращения к своим объектам. Поэтому у нас есть особый формат для ссылок в баннерах:

* **Страница** *index.php?dispatch=pages.view&page_id=23*

* **Товар:** *index.php?dispatch=products.view&product_id=230*

* **Категория:** *index.php?dispatch=categories.view&category_id=174*

* **Продавец:** *index.php?dispatch=companies.products&company_id=2*

* **Заказ:** *index.php?dispatch=orders.details&order_id=115* (только если покупатель авторизован)

* **Профиль:** *index.php?dispatch=profiles.update&user_id=3* (только если покупатель авторизован)

Например, чтобы сослаться в баннере на товар #248, введите следующее значение в поле **URL**:

.. code-block:: none

    index.php?dispatch=products.view&product_id=248

.. fancybox:: img/mobile_app_banners.png
    :alt: Устанавливаем для баннера URL, который будет работать и в Multi-Vendor, и в мобильном приложении.

.. hint::

    Этот формат ссылок также работает у баннеров в главном магазине и не зависит от изменений URL (например, если изменится доменное имя, магазин переедет в другую подпапку, или изменится SEO-имя объекта).

-----------------------------------------------------------
Домашняя страница: Как скрыть или показать названия блоков?
-----------------------------------------------------------

Названия блоков на главной странице приложения могут появляться, а могут не появляться. Это зависит от оболочки, которую вы выберете для блока в панели администратора вашего магазина.

Откройте страницу **Дизайн → Макеты** и выберите макет **MobileAppLayout**. Перейдите на вкладку **Homepage** и нажмите на иконку шестерёнки у нужного блока, чтобы открыть его настройки. Так вы сможете выбрать оболочку для блока:

* Выберите ``--``, если хотите скрыть заголовок блока на домашней странице в приложении.

* Выберите любую другую оболочку, если хотите, чтобы заголовок отображался.

  .. fancybox:: img/wrappers.png
      :alt: Оболочка блока в Multi-Vendor определяет, появится ли заголовок у блока на домашней странице в мобильном приложении.

--------------------------------------------------------
Боковая панель: Как добавлять или удалять элементы меню?
--------------------------------------------------------

Верхнее меню боковой панели (Главная, Корзина, Отложенные товары, Мой профиль, Заказы) всегда остаётся неизменным. Нижнее меню можно настроить из панели администратора вашего магазина.

#. Откройте страницу **Дизайн → Макеты**.

#. Выберите справа макет **MobileAppLayout**.

#. Перейдите на вкладку **Sidebar menu**.

#. Нажмите на иконку с изображением шестерёнки у блока **Pages**.

#. Откроются настройки блока. Перейдите на вкладку **Контент**. Здесь вы сможете выбрать страницы, которые должны появиться в боковой панели мобильного приложения.

   .. fancybox:: img/sidebar_menu.png
       :alt: Элементы меню в Multi-Vendor и в мобильном приложении.
