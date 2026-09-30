(function transformRow(source, target, map, log, isUpdate) {

    // Import Branch value
    if (source.u_branch == 'EEE') {
        target.u_branch = 'EEE';
    }
    else if (source.u_branch == 'ECE') {
        target.u_branch = 'ECE';
    }
    else if (source.u_branch == 'CSE') {
        target.u_branch = 'CSE';
    }

    // Map student details
    target.u_student_name = source.u_student_name;
    target.u_email = source.u_email;
    target.u_phone_number = source.u_phone_number;

})(source, target, map, log, action === "update");
