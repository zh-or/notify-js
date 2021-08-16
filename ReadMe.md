## 使用

`
const TEST_KEY = 'TEST_KEY';
notify.lock(TEST_KEY).wait(2000)
    .then(arg => {
        //arg = {a: 1}
        console.log('recv notify', arg);
    })
    .catch(e => {
        console.error(e);
    })
    
//...

notify.notify(TEST_KEY, {a: 1});
`
