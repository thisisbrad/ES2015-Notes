const name = 'Brad';
let age = 30;
const dateOfBirth = '07/11/1986';

/**
	* Using Const and Let makes reading the code easy to glance at and figure out.
	* const lets you know which variable change and which ones don't ever change.
*/

const statuses = [ 
  { code: 'OK', response: 'Request successful' },
  { code: 'FAILED', response: 'There was an error with your request' },
  { code: 'PENDING', response: 'Your reqeust is still pending' }
];
let message = '';
let currentCode = 'OK';

for (var i = 0; i < statuses.length; i++) {
  if (statuses[i].code === currentCode) {
    message = statuses[i].response;
  }
}