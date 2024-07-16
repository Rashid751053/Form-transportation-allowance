function createTransportationSurveyForm() {
  var form = FormApp.create('Al Bawani Ltd - Transportation Allowance vs. Vehicle Survey')
    .setDescription('This survey aims to gather information on the transportation preferences of employees in the Transportation Department at Al Bawani Ltd. Please fill out the form to indicate whether you are using the transportation allowance or prefer a company vehicle. Your input is crucial for our planning and logistics.');

  form.addTextItem()
    .setTitle('Employee Name')
    .setRequired(true);

  form.addTextItem()
    .setTitle('Badge Number')
    .setRequired(true);

  form.addTextItem()
    .setTitle('Project/Department')
    .setRequired(true);

  form.addMultipleChoiceItem()
    .setTitle('Transportation Preference')
    .setChoiceValues(['Transportation Allowance', 'Company Vehicle'])
    .setRequired(true);

  form.addTextItem()
    .setTitle('Signature')
    .setRequired(true);

  form.addDateItem()
    .setTitle('Date')
    .setRequired(true);

  Logger.log('Form URL: ' + form.getPublishedUrl());
}
