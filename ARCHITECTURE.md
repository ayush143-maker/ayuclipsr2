# Architecture
Pages serves the UI; Pages Functions are the API; D1 stores project/activity data; R2 stores private media; Queues coordinate work. FFmpeg must run outside Workers. Upload and worker hand-off still require implementation and real-device testing.
