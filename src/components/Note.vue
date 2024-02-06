<template>
  <div class="note">
    <p>Current price</p>

    <div>
      <img src="../assets/images/note_body_icon.svg" />
      <p>1.92<span>($5,822.47)</span></p>
    </div>

    <div>
      <img src="../assets/images/note_avatar.svg" />
      <p>Wade Warren</p>
    </div>
  </div>
</template>

<style>
.note {
  color: #fff;
  font-weight: 700;
  display: flex;
  flex-direction: column;
  gap: 20px;
  bottom: 100px;
  right: 100px;
  position: absolute;
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),
    linear-gradient(140.08deg, #9cd2ee 3.42%, #00acee 95.98%);
  box-shadow: -46px -61px 36px rgba(0, 0, 0, 0.25);
  border-radius: 10px;
  padding: 50px;
}

.note:hover {
  cursor: pointer;
  transform: scale(1.01);
  transition: 0.2s;
}

.note p {
  color: #fff;
  font-weight: 700;
}

.note div {
  display: flex;
  gap: 15px;
  align-items: center;
}

.note span {
  margin-left: 10px;
}
</style>
