# const-app-require-electron-app.on-certificate-error-event-webContents-url-error-ce
const { app } = require('electron')  app.on('certificate-error', (event, webContents, url, error, certificate, callback) => {   if (url === 'https://github.com') {     // Verification logic.     event.preventDefault()     callback(true)   } else {     callback(false)   } })
