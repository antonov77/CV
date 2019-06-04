<template>
  <div class="main-wrapper">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none">Резюме</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="./assets/profile.jpg" alt="">
        </span>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">Обо мне</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">Опыт</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Образование</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Навыки</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">Хобби</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#awards">Курсы</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">

      <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <h1 class="mb-0">{{ name }}
            <span class="text-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">{{ address }}
            <a href="mailto:name@email.com">{{ email }}</a>
          </div>
          <p class="mb-5">{{ aboutMe }}</p>
          <ul class="list-inline list-social-icons mb-0">
            <li class="list-inline-item">
              <a href="https://www.facebook.com/andrey.antonov.9279" target="_blank">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-facebook fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://github.com/antonov77" target="_blank">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
          <h2 class="mb-5">Опыт</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="job in experience" :key="job.description">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ job.position }}</h3>
              <div class="subheading mb-3">{{ job.company }}</div>
              <p>{{ job.description }}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
            </div>
          </div>

        </div>

      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="education">
        <div class="my-auto">
          <h2 class="mb-5">Образование</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">Волгоградский государственный университет</h3>
              <div class="subheading mb-3">1995-2000</div>
              <div>Радиофизика и электроника</div>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">August 2006 - May 2010</span>
            </div>
          </div>

        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">Навыки</h2>

          <div class="subheading mb-3">Кроссплатформенная разработка</div>
          <ul class="list-inline list-icons">
          <li class="list-inline-item">
              <i class="devicons devicons-html5"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-css3"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-sass"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-bootstrap"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-javascript"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-jquery"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-react"></i>
          </li>
            <li class="list-inline-item">
              <i class="devicons devicons-python"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-django"></i>
            </li>
          <li class="list-inline-item">
              <i class="devicons devicons-php"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-wordpress"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-ruby"></i>
            </li>
          </ul>
        <div class="subheading mb-3">Базы данных</div>
        <ul class="list-inline list-icons">
          <li class="list-inline-item">
              <i class="devicons devicons-mysql"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-postgresql"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-mongodb"></i>
            </li>
        </ul>
        <div class="subheading mb-3">Дизайн</div>
        <ul class="list-inline list-icons">
          <li class="list-inline-item">
              <i class="devicons devicons-photoshop"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-envato"></i>
            </li>
        </ul>
        <div class="subheading mb-3">Инструменты</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item">
              <i class="devicons devicons-jira"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-trello"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-npm"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-github"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-bitbucket"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-aws"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-heroku"></i>
            </li>
          </ul>
          <div class="subheading mb-3">Рабочий процесс</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
              Адаптивный дизайн</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Кросс-браузерное тестирование и отладка</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Работа в кросс-функциональной команде</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Гибкая разработка и Scrum</li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="interests">
        <div class="my-auto">
          <h2 class="mb-5">Хобби</h2>
          <p>Робототехника</p>
          <p>Теннис</p>
          <p class="mb-0">Фитнес</p>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="awards">
        <div class="my-auto">
          <h2 class="mb-5">Курсы</h2>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <a href="http://robotosha.ru/wp-content/uploads/2014/10/Coursera_Certificate_v1-9713821661055.pdf" target="_blank">Web Application Architectures</a> - University of New Mexico - 2014</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <a href="http://robotosha.ru/wp-content/uploads/2014/10/Coursera_Certificate_v1-9714891661055.pdf" target="_blank">Machine Learning</a> - Stanford University - 2014</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
            <a href="http://robotosha.ru/wp-content/uploads/2014/10/Coursera_Certificate_v1-9717301661055.pdf" target="_blank">Introduction to LaTEX</a> - Higher School of Economics - 2014</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <a href="http://robotosha.ru/wp-content/uploads/2014/10/Coursera_Certificate_v1-9709401661055.pdf" target="_blank">Computing for Data Analysis</a> - Johns Hopkins University - 2013</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <a href="http://robotosha.ru/wp-content/uploads/2014/10/Coursera_Certificate_v1-9703911661055.pdf" target="_blank">An Introduction to Interactive Programming in Python</a> - Rice University - 2013</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <a href="https://verify.edx.org/cert/6b0cf59d49ef4ebcb7194214eb12a543" target="_blank">AUTONAVx: Autonomous Navigation for Flying Robots</a> - Technische Universität München - 2015</li>
          </ul>
        </div>
      </section>

    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'Резюме',
      name: 'АНДРЕЙ',
      surname: 'АНТОНОВ',
      address: 'Волгоград · Россия · +7 (905) 334-51-19 ·',
      email: 'volgograd@list.ru',
      aboutMe: 'Обладаю большим опытом управления в том числе с использованием Agile-методик.',
      experience: [
        {
          position: 'Технический директор',
          company: 'Лаборатория цифровой медицины',
          description: 'Управление разработкой системами поддержки принятия врачебных решений (СППВР) с использованием методов Deep Learning для обработки медицинских изображений (маммограммы), методов NLP, релевантного поиска. Разработка системы распознавания изображений с использованием параллельных вычислений на GPU. Разработка медицинских приборов.Разработка ПО для работы с геномными данными.Разработка PWA-приложений.',
          startDate: 'Декабрь 2018',
          endDate: 'Настоящее время'
        },
        {
          position: 'Основатель стартапа',
          company: 'Робототехнический стартап Микроид',
          description: 'Разработка программируемых smart toys. Проект находится в стадии разработки.Разработка электроники, встраиваемого ПО, прикладного ПО.Аппаратное обеспечение: СнК на базе МК с архитектурой ARM Cortex F4, оптические датчики, датчики цвета и жестов, Bluetooth 5.0, NFC, ИНС, RGB-светодиоды, RGB OLED-дисплей, цифровой микрофон, лазерный дальномер, микрошаговые моторы. Встраиваемое ПО: проприетарная СРВ',
          startDate: 'Декабрь 2015',
          endDate: 'Настоящее время'
        },
        {
          position: 'Фрилансер',
          company: 'Спецприбор',
          description: 'Фулстек разработчик встраиваемых систем (аппаратное и программное обеспечение).Цифровая и аналоговая схемотехника, проектирование печатных плат. Разработка полной технической документации для массового производства. Система Motion capture (на базе ИНС), лазерный доплеровский виброметр, светодиодные информационные системы, система измерения наполненности стеклотары. Архитектуры МК: ARM Cortex, PIC, AVR',
          startDate: 'Май 2013',
          endDate: 'Декабрь 2015'
        },
        {
          position: 'Генеральный директор',
          company: 'Мегаполис',
          description: 'Компания по производству наружной рекламы и оказания услуг в области широкоформатной печати. Операционный менеджмент производственной компании. Внедрение системы «Бережливое производство» (TPS). Организация процессов управления качеством.',
          startDate: 'Март 2010',
          endDate: 'Май 2013'
        },
        {
          position: 'Технический директор',
          company: 'Мегаполис',
          description: 'Компания по производству наружной рекламы и оказания услуг в области широкоформатной печати. Организация и оптимизация производственных процессов. Разработка продукта и организация массового производства светодиодных информационных табло и экранов.',
          startDate: 'Декабрь 2007',
          endDate: 'Март 2010'
        },
        {
          position: 'Генеральный директор',
          company: 'Студия компьютерной графики и анимации «Зебра»',
          description: 'Управление компанией, занимающейся производством компьютерной графики, анимации и видеопродукции. Разработка дополнительных модулей для Maya, 3DS Max (трассировка лучей, быстрый рендеринг, моделирование физики частиц).',
          startDate: 'Май 2000',
          endDate: 'Декабрь 2007'
        },
        {
          position: 'Технический директор',
          company: 'Телеканал «Муниципальное телевидение Волгограда»',
          description: 'Перевод производства на цифровой формат выпуска и вещания ТВ-продукции. Оптимизация производственных процессов. Разработка ПО « Телесуфлер».',
          startDate: 'Август 1999',
          endDate: 'Февраль 2000'
        }
      ]
    }
  },
  mounted () {
    const $ = this.jquery
    this.$nextTick(() => {
      // our custom jQuery code goes here
      $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function () {
        if (location.pathname.replace(/^\//, '') === this.pathname.replace(/^\//, '') && location.hostname === this.hostname) {
          var target = $(this.hash)
          target = target.length ? target : $('[name=' + this.hash.slice(1) + ']')
          if (target.length) {
            $('html, body').animate({
              scrollTop: (target.offset().top)
            }, 1000, 'easeInOutExpo')
            return false
          }
        }
      })

      // Closes responsive menu when a scroll trigger link is clicked
      $('.js-scroll-trigger').click(function () {
        $('.navbar-collapse').collapse('hide')
      })

      // Activate scrollspy to add active class to navbar items on scroll
      $('body').scrollspy({
        target: '#sideNav'
      })
    })
  }
}
</script>

<style>
body {
  font-family: 'Helvetica', serif;
  padding-top: 54px;
  color: #868e96;
}

@media (min-width: 992px) {
  body {
    padding-top: 0;
    padding-left: 17rem;
  }
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Roboto', serif;
  font-weight: 700;
  text-transform: uppercase;
  color: #343a40;
}

h1 {
  font-size: 6rem;
  line-height: 5.5rem;
}

h2 {
  font-size: 3.5rem;
}

.subheading {
  text-transform: uppercase;
  font-weight: 500;
  font-family: 'Roboto', serif;
  font-size: 1.35rem;
}

.list-social-icons a {
  color: #495057;
}

.list-social-icons a:hover {
  color: #BD5D38;
}

.list-social-icons a .fa-lg {
  font-size: 1.75rem;
}

.list-icons {
  font-size: 3rem;
}

.list-icons .list-inline-item i:hover {
  color: #BD5D38;
}

#sideNav .navbar-nav .nav-item .nav-link {
  font-weight: 600;
  text-transform: uppercase;
}

@media (min-width: 992px) {
  #sideNav {
    text-align: center;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    width: 17rem;
    height: 100vh;
  }
  #sideNav .navbar-brand {
    display: flex;
    margin: auto auto 0;
    padding: 0.5rem;
  }
  #sideNav .navbar-brand .img-profile {
    max-width: 10rem;
    max-height: 10rem;
    border: 0.5rem solid rgba(255, 255, 255, 0.2);
  }
  #sideNav .navbar-collapse {
    display: flex;
    align-items: flex-start;
    flex-grow: 0;
    width: 100%;
    margin-bottom: auto;
  }
  #sideNav .navbar-collapse .navbar-nav {
    flex-direction: column;
    width: 100%;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item {
    display: block;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item .nav-link {
    display: block;
  }
}

section.resume-section {
  border-bottom: 1px solid #dee2e6;
  padding-top: 5rem !important;
  padding-bottom: 5rem !important;
}

section.resume-section .resume-item .resume-date {
  min-width: none;
}

@media (min-width: 768px) {
  section.resume-section {
    min-height: 100vh;
  }
  section.resume-section .resume-item .resume-date {
    min-width: 18rem;
  }
}

@media (min-width: 992px) {
  section.resume-section {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }
}

.bg-primary {
  background-color: #BD5D38 !important;
}

.text-primary {
  color: #BD5D38 !important;
}

a {
  color: #BD5D38;
}

a:hover, a:focus, a:active {
  color: #824027;
}
</style>
