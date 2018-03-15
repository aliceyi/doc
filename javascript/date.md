function addMonth (sd, num)  {
    // 根据开始时间和租期计算结束时间
    const self = this;
    const d = t.getd(sd);
    num = num >= 0 ? +num : 0;
    // 当前月份
    const oldMonth = d.getMonth();
    // 当前几号
    const oldDay = d.getDate();
    // 加月，设置月为：当前月份+要加的月数
    d.setDate(1);
    d.setMonth(oldMonth + num);
    let daysInMonth = new Date(d.getFullYear(), d.getMonth()+num, 0).getDate();
    d.setDate(Math.min(oldDay, daysInMonth));
    if (oldDay < daysInMonth) {
      d.setDate(oldDay -1);
    }
    // 输出时间戳
    return d;
  }