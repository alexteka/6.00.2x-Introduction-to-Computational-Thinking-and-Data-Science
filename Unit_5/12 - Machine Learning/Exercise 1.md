def lecture_activities(N, aLecture):
  lectureList=[]
  for num in range(N):
    flag = True
    lectureCount = 0

    while flag:
      if aLecture.get_listen_prob() != 1 pr aLecture.get_sleep_prob() != 1 or aLecture.get_fb_prob() != 1:
        lectureCount += 1
      else:
        flag = False
        lectureList.append(lectureCount)
    mean,std = get_mean_and_std(lectureList)
    width = 1.96*std
    return (mean, width)
