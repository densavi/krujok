<script>
import './Appointment.scss';
import PhotoSlider from "@/components/PhotoSlider/PhotoSlider.vue";
export default {
  name: "Appointment",
  components: {PhotoSlider},
}
</script>

<template>
  <div class="container">
    <div class="appointment">
      <div class="block appointment__info">
        <h1 class="appointment__title">Ваша запись</h1>
        <div class="appointment__descr">
          Услуги стоматолога - 2000 руб. <br>
          Продолжительность - 30 мин
        </div>
        <div class="appointment__date">
          <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" fill="none" viewBox="0 0 14 14">
            <g clip-path="url(#a)">
              <path fill="#175FFF" d="M7 7.382a.536.536 0 1 0 .536.536A.52.52 0 0 0 7 7.382Zm2.498 0a.536.536 0 1 0 .535.536.52.52 0 0 0-.535-.536Zm-4.994 0a.536.536 0 1 0 .536.537.52.52 0 0 0-.536-.537ZM7 9.85a.536.536 0 1 0 .536.535A.52.52 0 0 0 7 9.85Zm2.498 0a.536.536 0 1 0 .535.535.521.521 0 0 0-.535-.535Zm-4.994 0a.536.536 0 1 0 .536.535.518.518 0 0 0-.536-.535Z"/>
              <path fill="#175FFF" d="M10.695.911h-.887V.535A.573.573 0 0 0 9.268 0a.536.536 0 0 0-.537.535v.376h-3.46V.535A.573.573 0 0 0 4.728 0a.536.536 0 0 0-.535.535v.376h-.886A3.31 3.31 0 0 0 0 4.221v6.47A3.315 3.315 0 0 0 3.307 14h7.388A3.308 3.308 0 0 0 14 10.691v-6.47a3.314 3.314 0 0 0-3.305-3.31Zm0 12.017H3.307A2.235 2.235 0 0 1 1.07 10.69V5.676h11.86v5.015a2.24 2.24 0 0 1-2.234 2.237ZM3.307 1.983h.886v.401a.573.573 0 0 0 .535.537.538.538 0 0 0 .537-.537v-.4H8.73v.4a.574.574 0 0 0 .536.537.536.536 0 0 0 .535-.537v-.4h.887a2.237 2.237 0 0 1 2.24 2.237v.383H1.07v-.383a2.242 2.242 0 0 1 2.236-2.238Z"/>
            </g>
            <defs>
              <clipPath id="a">
                <path fill="#fff" d="M0 0h14v14H0z"/>
              </clipPath>
            </defs>
          </svg>
          14.07.2024 15:30
        </div>
        <div class="appointment__btn-group">
          <a href="#" class="btn">Перенести</a>
          <a href="#" class="btn btn-red">Отменить</a>
        </div>
      </div>
      <PhotoSlider />
      <a href="#" class="btn btn-big">Новая запись</a>
    </div>
  </div>
</template>