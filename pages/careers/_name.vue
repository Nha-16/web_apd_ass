<template>
  <div class="container">
    <v-card class="mx-auto" width="auto">
      <v-list-item three-line>
        <v-list-item-content>
          <div class="text-overline mb-4">
            <v-chip class="ma-2" color="primary"> Phnom Penh </v-chip>
            <v-chip class="ma-2" color="primary"> Full-Time </v-chip>
          </div>
          <v-list-item-title class="text-h5 mb-1">
            {{ job.title }}
          </v-list-item-title>
          <v-list-item-subtitle>{{ job.subtitle }}</v-list-item-subtitle>
          <h3 class="mt-4">Job Description</h3>
          <ul>
            <li class="mt-2" v-for="li in job.job_description" :key="li">
              {{ li }}
            </li>
          </ul>
          <h3 class="mt-4">Job Requirements</h3>
          <ul>
            <li class="mt-2" v-for="li in job.job_requirements" :key="li">
              {{ li }}
            </li>
            <v-card-actions class="mt-4">
              <v-btn text class="btn" color="success"> APPLY NOW </v-btn>
            </v-card-actions>
          </ul>
        </v-list-item-content>
      </v-list-item>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'DetailPage',
  data() {
    return {
      dialog: false,
      paramsData: this.$route.params.name,
      job: [],
      jobs: [
        {
          id: '1',
          slug: 'customer-service-officer',
          title: 'CUSTOMER SERVICE OFFICER',
          subtitle: 'OPERATIONS DEPARTMENT',
          job_description: [
            'Authorize over the counter services (Account opening, Withdrawal, Deposit, Foreign Exchange, Internal fund transfer, International fund transfer, close account, other request letter of request);',
            'Attend to customers’ needs and queries on the Bank’s products and services, and direct them to available resources for assistance, if required;',
            'Attend to all customer enquiries, feedback and complaints;',
            'Perform and handle customers’ deposits and withdrawals, changing money, sell money orders and traveler’s cheques, accept repayment for loans, payment for utilities bills or any other banking services;',
            'Insure complaints are resolved expediently and to customers’ satisfaction;',
            'Provide an accurate, efficient and quality service that exceeds the customer’s expectations;',
            'Serve as a clarifying reference person and information point of contact, directing persons and incoming calls to appropriate persons and departments;',
            'Observe and comply at all times with all acts, laws, articles of associations, rules and regulations affecting the Bank’s business and be conversant with all statutory modifications and reenactments as may be introduced thereto;',
            'Ensure compliance with relevant Acts, Laws, Rules of the National Bank of Cambodia, directives and guidelines issued by the regulatory bodies and the Bank’s internal policies and procedures;',
            'Display teamwork and work closely with other colleagues at all times;',
            'Perform any special order by Management.',
          ],
          job_requirements: [
            'Holding bachelor degree in Finance and Banking or equivalent professional qualifications;',
            'Cash handling experience and on-the-job training may be required;',
            'High level of accountability, efficiency, and accuracy;',
            'Minimum one-year experience from related file or banking experience is an advantage;',
            'High proficiency spoken and written of English;',
            'Professional appearance and courteous manner;',
            'Committed, hard-working, and honest individual;',
            'Willing to work under pressure.',
          ],
        },

        {
          id: '2',
          slug: 'assistant-it-security-analyst-manager',
          title: 'ASSISTANT IT SECURITY ANALYST MANAGER',
          subtitle: 'IT DEPARTMENT',
          job_description: [
            'Initiate, lead and coordinate actions to strengthen and monitor information security and cyber security controls.',
            'Undertake information security review in businesses and functions to ensure compliance with internal policies and external regulations;',
            'Respond to and investigate information security incidents and breaches in order to reduce/contain potential damage.',
            'Act as liaison with relevant regulators and/or enforcement agencies in relation to information security matters.',
            'Perform periodic assessment and provide information for risk profiling reporting.',
            'Perform security and risk assessment based on Cyber Resilience Assessment Framework.',
            'Develop the relevant staff with the right kinds and level of skill.',
            'Monitor the service quality of the team & ensure team members have strictly followed the standard regulatory requirements.',
            'Oversee information security audits, whether performed by an organization or third-party personnel.',
            'Manage and configure physical security, disaster recovery, and data backup systems.',
            'Provide training to information security personnel during onboarding.',
            'Evaluate department budget and costs associated with technological training.',
            'Assess current technology architecture for vulnerabilities, weaknesses, and for possible upgrades or improvement.',
            'Other tasks assigned by Manager/HOD',
          ],
          job_requirements: [
            "Bachelor's Degree holder in IT, Computer Science/ Cyber Security, or equivalent professional qualifications.",
            'Certified in CISA or related professional certification.',
            'In-depth knowledge in IT security services',
            'Ability to communicate effectively with senior management and other departments',
            'Creative, dynamic, flexible, self‐direct, and self‐motivated team player',
            'High proficiency spoken and written of English/ Chinese is a plus',
            'Autonomous, quick learner, and pro‐active',
            'Effective communication and management skills',
            'At least 5 years in technology audit or cyber and information security.',
            'At least 3 years in a team lead/management role',
          ],
        },

        {
          id: '3',
          slug: 'assistant-it-security-compliance-manager',
          title: 'ASSISTANT IT SECURITY ANALYST MANAGER',
          subtitle: 'IT DEPARTMENT',
          job_description: [
            'Initiate, lead and coordinate actions to strengthen and monitor information security and cyber security controls.',
            'Undertake information security review in businesses and functions to ensure compliance with internal policies and external regulations;',
            'Respond to and investigate information security incidents and breaches in order to reduce/contain potential damage.',
            'Act as liaison with relevant regulators and/or enforcement agencies in relation to information security matters.',
            'Perform periodic assessment and provide information for risk profiling reporting.',
            'Perform security and risk assessment based on Cyber Resilience Assessment Framework.',
            'Develop the relevant staff with the right kinds and level of skill.',
            'Monitor the service quality of the team & ensure team members have strictly followed the standard regulatory requirements.',
            'Oversee information security audits, whether performed by an organization or third-party personnel.',
            'Manage and configure physical security, disaster recovery, and data backup systems.',
            'Provide training to information security personnel during onboarding.',
            'Evaluate department budget and costs associated with technological training.',
            'Assess current technology architecture for vulnerabilities, weaknesses, and for possible upgrades or improvement.',
            'Other tasks assigned by Manager/HOD',
          ],
          job_requirements: [
            "Bachelor's Degree holder in IT, Computer Science/ Cyber Security, or equivalent professional qualifications.",
            'Certified in CISA or related professional certification.',
            'In-depth knowledge in IT security services',
            'Ability to communicate effectively with senior management and other departments',
            'Creative, dynamic, flexible, self‐direct, and self‐motivated team player',
            'High proficiency spoken and written of English/ Chinese is a plus',
            'Autonomous, quick learner, and pro‐active',
            'Effective communication and management skills',
            'At least 5 years in technology audit or cyber and information security.',
            'At least 3 years in a team lead/management role',
          ],
        },

        {
          id: '4',
          slug: 'senior-officer-digital-marketing',
          title: 'SENIOR OFFICER, DIGITAL MARKETING',
          subtitle: 'DIGITAL MARKETING DEPARTMENT',
          job_description: [
            'Assist in the formulation of strategies to build a lasting digital connection with consumers',
            'Design, manage and implement a social media marketing strategy to ensure that objectives are met to maximum efficiency',
            'Propose and produce weekly content',
            'Coordinate with a designer for designing the weekly content.',
            'Propose campaign and strategy to ensure the APD Bank’s social media is actively and effectively engaged with audiences',
            'Tracking and monitoring campaigns’ performances and campaign ROI',
            'Research advertising trends and competitor’s analysis',
            'Acquire insight into online marketing trends and keep strategies up-to-date',
            'Work with external agencies to ensure objectives and goals are met and make recommendations to further improve all stages of communication on social media',
            'Good understanding of Facebook Ad Management and marketing funnel',
            'Support additional marketing and communication projects',
            'Engage and coordinate with stakeholders with journalists for the interview',
            'Prepare the script and answer key speaker',
            'Produce the press release and coordinate video story',
            'Prepare the content for each product',
            'CSR Activities, Execute the CSR projects that align with APD core value',
            'Coordinate the shooting plan with the protagonist, the production team',
          ],
          job_requirements: [
            'Degree in Marketing, Advertising or other related fields',
            'At least 2 years experience working on with the digital platform, content management, and paid-ads digitally',
            'Knowledge in the marketing',
            'Content management and content writing',
            'Experience working with digital media agencies',
            'Knowledge of graphic design principles and copywriting',
            'Knowledge of digital marketing tools and social media platforms',
            'Basic knowledge of digital channels (Google SEO, Google Analytics, Facebook Ads Manager…etc)',
            'Ability to think creatively and innovatively',
          ],
        },

        {
          id: '5',
          slug: 'operations-officer',
          title: 'OPERATIONS OFFICER',
          subtitle: 'OPERATIONS DEPARTMENT',
          job_description: [
            'Authorize over the counter services (Account opening, Withdrawal, Deposit, Foreign Exchange, Internal fund transfer, International fund transfer, close account, other request letter of request)',
            'Introduce bank’s product and services to customers including Deposit and Loan',
            'Handle and solve customer calls, inquiry and complaints',
            'Approve on ATM Card creation and ATM Cash counting and Loading',
            'Control cheques, collecting cheque book from branches, clear local cheques report cheque clearing, deposit and inward cheques',
            'Authorize to update CIF on core banking system',
            'Check daily report (counter report, Account open, letter of request, marketing report for BM) that receive from Teller',
            'Daily open and close counter & Branch operation on system',
            'Ensure staff training and compliance with procedures',
            'Check daily cash count with teller and ensure that cash is balance with report',
            'Maintain good customer relations and refer customers to appropriate staff for new services to promote business for the bank',
            'Responsible for vault room and all till’s tellers',
            'Perform any special order by Management',
          ],
          job_requirements: [
            'Holding bachelor degree in Finance and Banking or equivalent professional qualifications;',
            'Proven track record in delivering high quality results in short time frames;',
            'Possess superior communication and leadership skills;',
            'At least 3 years work experience in banking industry;',
            'High proficiency spoken and written of English;',
            'Creative, dynamic, flexible, self-direct and self-motivated team player;',
            'Committed, hard-working, and honest individual;',
            'Willing to work under pressure.',
          ],
        },
        {
          id: '6',
          slug: 'chief-cashier',
          title: 'OPERATIONS OFFICER',
          subtitle: 'OPERATIONS DEPARTMENT',
          job_description: [
            'Perform and handle customers’ deposits and withdrawals, changing money, sell money orders and traveler’s cheques, accept repayment for loans, payment for utilities bills or any other banking services',
            'Attend to customers’ enquiries on the various products and services of the Bank',
            'Observe and comply at all times with all acts, laws, articles of associations, rules and regulations affecting the Bank’s business and be conversant with all statutory modifications and reenactments as may be introduced thereto',
            'Ensure compliance with relevant Acts, Laws, Rules of National Bank of Cambodia, directives and guidelines issued by the regulatory bodies, Information Technology Security Standards Code and the Bank’s internal policies and procedures',
            'Perform special assignments or ad hoc projects as assigned from time to time',
            'Display teamwork and work closely with other senior management personnel at all times;',
            'Perform any special order by manager in charge.',
          ],
          job_requirements: [
            'Holding bachelor degree in Finance and Banking or equivalent professional qualifications',
            'Minimum 3 years of working experience in financial institutions; Banking is an advantage',
            'Cash handling experience is priority',
            'High level of accountability, efficiency, and accuracy',
            'High proficiency spoken and written of English',
            'Professional appearance and courteous manner',
            'Committed, hard-working, and honest individual',
            'Willing to work under pressure.',
          ],
        },
      ],
    }
  },
  created() {
    this.job = this.jobs.find((i) => i.slug === this.paramsData)
    // console.log('lskfksjagfas',this.job);
  },
}
</script>
<style scoped>
.btn {
  background: #1976d2;
  color: #ffff !important;
}
</style>
