<template>
  <div>
    <section class="section-strong">
      <div class="section-strong__wrapper">
        <div class="section-strong__wrapper-left">
          <block-title align="start" tag="h1" title="Strong for life with us "/>
          <div class="section-strong__wrapper-left__subtitle">The best Pre/postnatal fitness app! 100 exercises divided
            in before, during
            and after pregnancy. Stay
            strong and healthy through all stages of pregnancy.
          </div>
          <div class="mobile-store_items">
            <NuxtLink to="https://play.google.com/store/apps?hl=ru&gl=US&pli=1">
              <img src="../public/images/app-store.svg" alt="app-store">
            </NuxtLink>
            <NuxtLink to="https://play.google.com/store/apps?hl=ru&gl=US&pli=1">
              <img src="../public/images/play-market.svg" alt="play-market">
            </NuxtLink>
          </div>
        </div>
        <div class="section-strong__wrapper-right">

        </div>
      </div>
    </section>

    <section class="section-how-it-work">
      <block-title align="center" tag="h2" subtitle="Easy, fun & essential training for moms"
                   title="How does it work?"/>
      <div class="how-it-work">
        <div class="how-it-work__item">
          <div>
            <img src="../public/images/icons/icon-search.svg" alt="icon search">
          </div>
          <div>
            <div class="block-title__subtitle">
              Browse exercises
            </div>
            <div class="how-it-work__description">
              Browse over 100 exercises with a video or picture and a description.
            </div>
          </div>

        </div>
        <div class="how-it-work__item">
          <div>
            <img src="../public/images/icons/icon-share.svg" alt="icon share">
          </div>
          <div>
            <div class="block-title__subtitle">
              Create timeline
            </div>
            <div class="how-it-work__description">
              Take pictures along the way during and after the pregnancy to see the transformation.
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section-before-during">
      <block-title align="center" tag="h2"
                   subtitle="The app is divided into three different stages to help you choose appropriate exercises. Each exercise is carefully selected to ensure safe and appropriate adjustments to follow the pregnancy’s progress."
                   title="Before, during and after pregnancy"/>
      <div class="section-before-during__wrapper">
        <div class="before-during__item">
          <div class="before-during__item">
            <div class="before-during__item_info">
              <div class="title">Before pregnancy</div>
              <div class="underscore"></div>
              <div class="sub-title">Trimesters</div>
              <div class="description">The pregnancy is divided into first trimester, second trimester part 1 and 2, and
                third trimester part 1 and 2 to provide exercises that are safe for each stage of the pregnancy. Each
                exercise comes with a video and a description so you can safely perform each exercise. Simple put in
                your due date and you will be taken to the proper stage.
              </div>
            </div>
          </div>
          <div class="before-during__item_img">
            <img src="../public/images/sec_before-druging/right_durging.png" alt="left_during">
          </div>
        </div>
        <div class="section-before-during__wrapper__bg">
        </div>
        <div class="before-during__item">
          <div class="before-during__item_img">
            <img src="../public/images/sec_before-druging/left_during.png" alt="right_during">
          </div>
          <div class="before-during__item_info">
            <div class="title">During pregnancy</div>
            <div class="underscore"></div>
            <div class="description">Working out during pregnancy has many benefits for both the mom and the baby. It
              can reduce back pain, help prevent gestational diabetes, promote good posture, strength and endurance, and
              also improve the ability to cope with labor.
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section-blog">
      <block-title align="center" tag="h2" title="Our blog posts"/>
      <div class="section-blog__wrapper">
        <div class="section-blog__wrapper-post">
          <img src="../public/images/sec_posts/post_1.png" alt="post">
          <div class="section-blog__wrapper-post__info">
            <div class="title">Return to running after pregnancy – Is your body strong enough for running?</div>
            <div class="user-info">
              <img src="../public/images/sec_posts/posts_user_icon.svg" alt="user icon">
              <div class="user-name">BY TILDA LOFTIN</div>
              <div class="date-publish">JUNE 25, 2021</div>
            </div>
          </div>
        </div>
        <div class="section-blog__wrapper-posts__grid">
          <div class="section-blog__wrapper-posts__grid-item">
            <img src="../public/images/sec_posts/grid_2.png" alt="post">
            <div class="section-blog__wrapper-posts__grid-item-text">
              <div class="title">
                Stroller walks
              </div>
              <div class="date-publish">
                APRIL 21, 2021
              </div>
            </div>
          </div>
          <div class="section-blog__wrapper-posts__grid-item">
            <img src="../public/images/sec_posts/grid_3.png" alt="post">
            <div class="section-blog__wrapper-posts__grid-item-text">
              <div class="title">
                Playground workout
              </div>
              <div class="date-publish">
                MARCH 17, 2020
              </div>
            </div>
          </div>
          <div class="section-blog__wrapper-posts__grid-item">
            <img src="../public/images/sec_posts/grid_4.png" alt="post">
            <div class="section-blog__wrapper-posts__grid-item-text">
              <div class="title">
                Your Essential Fitness Gear for Each Trimester
              </div>
              <div class="date-publish">
                FEBRUARY 21, 2021
              </div>
            </div>
          </div>
          <div class="section-blog__wrapper-posts__grid-item">
            <img src="../public/images/sec_posts/grid_5.png" alt="post">
            <div class="section-blog__wrapper-posts__grid-item-text">
              <div class="title">
                What YOU could gain by working with a Woman’s Health Physical Therapist
              </div>
              <div class="date-publish">
                JANUARY 23, 2020
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="section-blog__link">
        <NuxtLink>
          Like what you see? View more <img src="../public/images/sec_posts/button_right.svg" alt="arrow">
        </NuxtLink>
      </div>
    </section>
    <section class="section-form">
      <div class="section-form__wrapper">
        <h2>Send your data</h2>
        <NuxtLink to="/form">Go to form</NuxtLink>
      </div>
    </section>
  </div>
</template>
